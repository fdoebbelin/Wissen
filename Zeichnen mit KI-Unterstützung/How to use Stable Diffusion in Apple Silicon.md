---
source: https://huggingface.co/docs/diffusers/optimization/mps
---
🤗 Diffusers is compatible with Apple silicon for Stable Diffusion inference, using the PyTorch `mps` device. These are the steps you need to follow to use your M1 or M2 computer with Stable Diffusion.

## [](https://huggingface.co/docs/diffusers/optimization/mps#requirements)Requirements

- Mac computer with Apple silicon (M1/M2) hardware.
- macOS 12.6 or later (13.0 or later recommended).
- arm64 version of Python.
- PyTorch 2.0 (recommended) or 1.13 (minimum version supported for `mps`). You can install it with `pip` or `conda` using the instructions in [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/).

## [](https://huggingface.co/docs/diffusers/optimization/mps#inference-pipeline)Inference Pipeline

The snippet below demonstrates how to use the `mps` backend using the familiar `to()` interface to move the Stable Diffusion pipeline to your M1 or M2 device.

**If you are using PyTorch 1.13** you need to “prime” the pipeline using an additional one-time pass through it. This is a temporary workaround for a weird issue we detected: the first inference pass produces slightly different results than subsequent ones. You only need to do this pass once, and it’s ok to use just one inference step and discard the result.

We strongly recommend you use PyTorch 2 or better, as it solves a number of problems like the one described in the previous tip.

Copied

from diffusers import DiffusionPipeline

pipe = DiffusionPipeline.from_pretrained("runwayml/stable-diffusion-v1-5")
pipe = pipe.to("mps")

# Recommended if your computer has < 64 GB of RAM
pipe.enable_attention_slicing()

prompt = "a photo of an astronaut riding a horse on mars"

# First-time "warmup" pass if PyTorch version is 1.13 (see explanation above)
_ = pipe(prompt, num_inference_steps=1)

# Results match those from the CPU device after the warmup pass.
image = pipe(prompt).images[0]

## [](https://huggingface.co/docs/diffusers/optimization/mps#performance-recommendations)Performance Recommendations

M1/M2 performance is very sensitive to memory pressure. The system will automatically swap if it needs to, but performance will degrade significantly when it does.

We recommend you use _attention slicing_ to reduce memory pressure during inference and prevent swapping, particularly if your computer has less than 64 GB of system RAM, or if you generate images at non-standard resolutions larger than 512 × 512 pixels. Attention slicing performs the costly attention operation in multiple steps instead of all at once. It usually has a performance impact of ~20% in computers without universal memory, but we have observed _better performance_ in most Apple Silicon computers, unless you have 64 GB or more.

Copied

pipeline.enable_attention_slicing()

## [](https://huggingface.co/docs/diffusers/optimization/mps#known-issues)Known Issues

- Generating multiple prompts in a batch [crashes or doesn’t work reliably](https://github.com/huggingface/diffusers/issues/363). We believe this is related to the [`mps` backend in PyTorch](https://github.com/pytorch/pytorch/issues/84039). This is being resolved, but for now we recommend to iterate instead of batching.

[←Core ML](https://huggingface.co/docs/diffusers/optimization/coreml)[Habana Gaudi→](https://huggingface.co/docs/diffusers/optimization/habana)

[How to use Stable Diffusion in Apple Silicon (M1/M2)](https://huggingface.co/docs/diffusers/optimization/mps#how-to-use-stable-diffusion-in-apple-silicon-m1m2)[Requirements](https://huggingface.co/docs/diffusers/optimization/mps#requirements)[Inference Pipeline](https://huggingface.co/docs/diffusers/optimization/mps#inference-pipeline)[Performance Recommendations](https://huggingface.co/docs/diffusers/optimization/mps#performance-recommendations)[K](https://huggingface.co/docs/diffusers/optimization/mps#known-issues)
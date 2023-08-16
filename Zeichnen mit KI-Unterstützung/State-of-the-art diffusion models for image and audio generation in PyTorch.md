---
source: https://github.com/huggingface/diffusers
---

🤗 Diffusers is the go-to library for state-of-the-art pretrained diffusion models for generating images, audio, and even 3D structures of molecules. Whether you're looking for a simple inference solution or training your own diffusion models, 🤗 Diffusers is a modular toolbox that supports both. Our library is designed with a focus on [usability over performance](https://huggingface.co/docs/diffusers/conceptual/philosophy#usability-over-performance), [simple over easy](https://huggingface.co/docs/diffusers/conceptual/philosophy#simple-over-easy), and [customizability over abstractions](https://huggingface.co/docs/diffusers/conceptual/philosophy#tweakable-contributorfriendly-over-abstraction).

🤗 Diffusers offers three core components:

- State-of-the-art [diffusion pipelines](https://huggingface.co/docs/diffusers/api/pipelines/overview) that can be run in inference with just a few lines of code.
- Interchangeable noise [schedulers](https://huggingface.co/docs/diffusers/api/schedulers/overview) for different diffusion speeds and output quality.
- Pretrained [models](https://huggingface.co/docs/diffusers/api/models) that can be used as building blocks, and combined with schedulers, for creating your own end-to-end diffusion systems.

## [](https://github.com/huggingface/diffusers#installation)Installation

We recommend installing 🤗 Diffusers in a virtual environment from PyPi or Conda. For more details about installing [PyTorch](https://pytorch.org/get-started/locally/) and [Flax](https://flax.readthedocs.io/en/latest/#installation), please refer to their official documentation.

### [](https://github.com/huggingface/diffusers#pytorch)PyTorch

With `pip` (official package):

```shell
pip install --upgrade diffusers[torch]
```

With `conda` (maintained by the community):

```shell
conda install -c conda-forge diffusers
```

### [](https://github.com/huggingface/diffusers#flax)Flax

With `pip` (official package):

```shell
pip install --upgrade diffusers[flax]
```

### [](https://github.com/huggingface/diffusers#apple-silicon-m1m2-support)Apple Silicon (M1/M2) support

Please refer to the [How to use Stable Diffusion in Apple Silicon](https://huggingface.co/docs/diffusers/optimization/mps) guide.

## [](https://github.com/huggingface/diffusers#quickstart)Quickstart

Generating outputs is super easy with 🤗 Diffusers. To generate an image from text, use the `from_pretrained` method to load any pretrained diffusion model (browse the [Hub](https://huggingface.co/models?library=diffusers&sort=downloads) for 4000+ checkpoints):

```python
from diffusers import DiffusionPipeline
import torch

pipeline = DiffusionPipeline.from_pretrained("runwayml/stable-diffusion-v1-5", torch_dtype=torch.float16)
pipeline.to("cuda")
pipeline("An image of a squirrel in Picasso style").images[0]
```

You can also dig into the models and schedulers toolbox to build your own diffusion system:

```python
from diffusers import DDPMScheduler, UNet2DModel
from PIL import Image
import torch
import numpy as np

scheduler = DDPMScheduler.from_pretrained("google/ddpm-cat-256")
model = UNet2DModel.from_pretrained("google/ddpm-cat-256").to("cuda")
scheduler.set_timesteps(50)

sample_size = model.config.sample_size
noise = torch.randn((1, 3, sample_size, sample_size)).to("cuda")
input = noise

for t in scheduler.timesteps:
    with torch.no_grad():
        noisy_residual = model(input, t).sample
        prev_noisy_sample = scheduler.step(noisy_residual, t, input).prev_sample
        input = prev_noisy_sample

image = (input / 2 + 0.5).clamp(0, 1)
image = image.cpu().permute(0, 2, 3, 1).numpy()[0]
image = Image.fromarray((image * 255).round().astype("uint8"))
image
```

Check out the [Quickstart](https://huggingface.co/docs/diffusers/quicktour) to launch your diffusion journey today!

## [](https://github.com/huggingface/diffusers#how-to-navigate-the-documentation)How to navigate the documentation

|**Documentation**|**What can I learn?**|
|---|---|
|[Tutorial](https://huggingface.co/docs/diffusers/tutorials/tutorial_overview)|A basic crash course for learning how to use the library's most important features like using models and schedulers to build your own diffusion system, and training your own diffusion model.|
|[Loading](https://huggingface.co/docs/diffusers/using-diffusers/loading_overview)|Guides for how to load and configure all the components (pipelines, models, and schedulers) of the library, as well as how to use different schedulers.|
|[Pipelines for inference](https://huggingface.co/docs/diffusers/using-diffusers/pipeline_overview)|Guides for how to use pipelines for different inference tasks, batched generation, controlling generated outputs and randomness, and how to contribute a pipeline to the library.|
|[Optimization](https://huggingface.co/docs/diffusers/optimization/opt_overview)|Guides for how to optimize your diffusion model to run faster and consume less memory.|
|[Training](https://huggingface.co/docs/diffusers/training/overview)|Guides for how to train a diffusion model for different tasks with different training techniques.|

## [](https://github.com/huggingface/diffusers#contribution)Contribution

We ❤️ contributions from the open-source community! If you want to contribute to this library, please check out our [Contribution guide](https://github.com/huggingface/diffusers/blob/main/CONTRIBUTING.md). You can look out for [issues](https://github.com/huggingface/diffusers/issues) you'd like to tackle to contribute to the library.

- See [Good first issues](https://github.com/huggingface/diffusers/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) for general opportunities to contribute
- See [New model/pipeline](https://github.com/huggingface/diffusers/issues?q=is%3Aopen+is%3Aissue+label%3A%22New+pipeline%2Fmodel%22) to contribute exciting new diffusion models / diffusion pipelines
- See [New scheduler](https://github.com/huggingface/diffusers/issues?q=is%3Aopen+is%3Aissue+label%3A%22New+scheduler%22)

Also, say 👋 in our public Discord channel [![Join us on Discord](https://camo.githubusercontent.com/6752f150c04aa4fb06db9d04d900329ef595a2376ea06860a1e834c89e5ab725/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f3832333831333135393539323030313533373f636f6c6f723d353836354632266c6f676f3d646973636f7264266c6f676f436f6c6f723d7768697465)](https://discord.gg/G7tWnz98XR). We discuss the hottest trends about diffusion models, help each other with contributions, personal projects or just hang out ☕.

## [](https://github.com/huggingface/diffusers#popular-tasks--pipelines)Popular Tasks & Pipelines

|Task|Pipeline|🤗 Hub|
|---|---|---|
|Unconditional Image Generation|[DDPM](https://huggingface.co/docs/diffusers/api/pipelines/ddpm)|[google/ddpm-ema-church-256](https://huggingface.co/google/ddpm-ema-church-256)|
|Text-to-Image|[Stable Diffusion Text-to-Image](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/text2img)|[runwayml/stable-diffusion-v1-5](https://huggingface.co/runwayml/stable-diffusion-v1-5)|
|Text-to-Image|[unclip](https://huggingface.co/docs/diffusers/api/pipelines/unclip)|[kakaobrain/karlo-v1-alpha](https://huggingface.co/kakaobrain/karlo-v1-alpha)|
|Text-to-Image|[if](https://huggingface.co/docs/diffusers/api/pipelines/if)|[DeepFloyd/IF-I-XL-v1.0](https://huggingface.co/DeepFloyd/IF-I-XL-v1.0)|
|Text-guided Image-to-Image|[Controlnet](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/controlnet)|[lllyasviel/sd-controlnet-canny](https://huggingface.co/lllyasviel/sd-controlnet-canny)|
|Text-guided Image-to-Image|[Instruct Pix2Pix](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/pix2pix)|[timbrooks/instruct-pix2pix](https://huggingface.co/timbrooks/instruct-pix2pix)|
|Text-guided Image-to-Image|[Stable Diffusion Image-to-Image](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/img2img)|[runwayml/stable-diffusion-v1-5](https://huggingface.co/runwayml/stable-diffusion-v1-5)|
|Text-guided Image Inpainting|[Stable Diffusion Inpaint](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/inpaint)|[runwayml/stable-diffusion-inpainting](https://huggingface.co/runwayml/stable-diffusion-inpainting)|
|Image Variation|[Stable Diffusion Image Variation](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/image_variation)|[lambdalabs/sd-image-variations-diffusers](https://huggingface.co/lambdalabs/sd-image-variations-diffusers)|
|Super Resolution|[Stable Diffusion Upscale](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/upscale)|[stabilityai/stable-diffusion-x4-upscaler](https://huggingface.co/stabilityai/stable-diffusion-x4-upscaler)|
|Super Resolution|[Stable Diffusion Latent Upscale](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/latent_upscale)|[stabilityai/sd-x2-latent-upscaler](https://huggingface.co/stabilityai/sd-x2-latent-upscaler)|

## [](https://github.com/huggingface/diffusers#popular-libraries-using--diffusers)Popular libraries using 🧨 Diffusers

- [https://github.com/microsoft/TaskMatrix](https://github.com/microsoft/TaskMatrix)
- [https://github.com/invoke-ai/InvokeAI](https://github.com/invoke-ai/InvokeAI)
- [https://github.com/apple/ml-stable-diffusion](https://github.com/apple/ml-stable-diffusion)
- [https://github.com/Sanster/lama-cleaner](https://github.com/Sanster/lama-cleaner)
- [https://github.com/IDEA-Research/Grounded-Segment-Anything](https://github.com/IDEA-Research/Grounded-Segment-Anything)
- [https://github.com/ashawkey/stable-dreamfusion](https://github.com/ashawkey/stable-dreamfusion)
- [https://github.com/deep-floyd/IF](https://github.com/deep-floyd/IF)
- [https://github.com/bentoml/BentoML](https://github.com/bentoml/BentoML)
- [https://github.com/bmaltais/kohya_ss](https://github.com/bmaltais/kohya_ss)
- +3000 other amazing GitHub repositories 💪

Thank you for using us ❤️
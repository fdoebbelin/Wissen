---
source: https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks
---
## Which GPU Runs AI Fastest (Updated)

By [Jarred Walton](https://www.tomshardware.com/author/jarred-walton)

published January 26, 2023

Which graphics card offers the fastest AI?

- [](https://www.facebook.com/sharer/sharer.php?u=https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks)

- [](https://twitter.com/intent/tweet?text=Stable%20Diffusion%20Benchmarked%3A%20Which%20GPU%20Runs%20AI%20Fastest%20%28Updated%29&url=https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks)
- [](https://www.reddit.com/submit?url=https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks&title=Stable%20Diffusion%20Benchmarked:%20Which%20GPU%20Runs%20AI%20Fastest%20(Updated))
- [](https://pinterest.com/pin/create/button/?url=https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks&media=https://cdn.mos.cms.futurecdn.net/JxtTd9NUa4poQXVFykHCBf-1200-80.jpg)
- [](https://share.flipboard.com/bookmarklet/popout?title=Stable%20Diffusion%20Benchmarked%3A%20Which%20GPU%20Runs%20AI%20Fastest%20%28Updated%29&url=https%3A%2F%2Fwww.tomshardware.com%2Fnews%2Fstable-diffusion-gpu-benchmarks)

- [](mailto:?subject=I%20found%20this%20webpage&body=Hi,%20I%20found%20this%20webpage%20and%20thought%20you%20might%20like%20it%20https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks)

[Comments (78)](https://www.tomshardware.com/news/stable-diffusion-gpu-benchmarks#xenforo-comments-3793737)

![Stable Diffusion sample images](https://cdn.mos.cms.futurecdn.net/4b6AqUCPq2QhdhigeuDMMg-320-80.jpg)

(Image credit: Tom's Hardware)

Artificial Intelligence and deep learning are constantly in the headlines these days, whether it be [ChatGPT generating poor advice](https://www.tomshardware.com/news/chatgpt-told-me-break-my-cpu), self-driving cars, artists being accused of using AI, medical advice from AI, and more. Most of these tools rely on complex servers with lots of hardware for training, but using the trained network via inference can be done on your PC, using its graphics card. But how fast are consumer GPUs for doing AI inference?  
  
We've benchmarked Stable Diffusion, a popular AI image creator, on the latest Nvidia, AMD, and even Intel GPUs to see how they stack up. If you've by chance tried to get Stable Diffusion up and running on your own PC, you may have some inkling of how complex — or simple! — that can be. The short summary is that Nvidia's GPUs rule the roost, with most software designed using CUDA and other Nvidia toolsets. But that doesn't mean you can't get Stable Diffusion running on the other GPUs.  
  
We ended up using three different Stable Diffusion projects for our testing, mostly because no single package worked on every GPU. For Nvidia, we opted for [Automatic 1111's webui version](https://github.com/AUTOMATIC1111/stable-diffusion-webui); it performed best, had more options, and was easy to get running. AMD GPUs were tested using [Nod.ai's Shark version](https://github.com/nod-ai/SHARK/blob/main/shark/examples/shark_inference/stable_diffusion/stable_diffusion_amd.md) — we checked performance on Nvidia GPUs (in both Vulkan and CUDA modes) and found it was... lacking. Getting Intel's Arc GPUs running was a bit more difficult, due to lack of support, but [Stable Diffusion OpenVINO](https://github.com/bes-dev/stable_diffusion.openvino) gave us some _very_ basic functionality.  
  
Disclaimers are in order. We didn't code any of these tools, but we did look for stuff that was easy to get running (under Windows) that also seemed to be reasonably optimized. We're relatively confident that the Nvidia 30-series tests do a good job of extracting close to optimal performance — particularly when xformers is enabled, which provides an additional ~20% boost in performance (though at reduced precision that may affect quality). RTX 40-series results meanwhile were lower initially, but George SV8ARJ [provided this fix](https://github.com/AUTOMATIC1111/stable-diffusion-webui/pull/5939#issuecomment-1368952030), where replacing the PyTorch CUDA DLLs gave a healthy boost to performance.

The AMD results are also a bit of a mixed bag: RDNA 3 GPUs perform very well while the RDNA 2 GPUs seem rather mediocre. Nod.ai let us know they're still working on 'tuned' models for RDNA 2, which should boost performance quite a bit (potentially double) once they're available. Finally, on Intel GPUs, even though the ultimate performance seems to line up decently with the AMD options, in practice the time to render is substantially longer — it takes 5–10 seconds before the actual generation task kicks off, and probably a lot of extra background stuff is happening that slows it down.  
  
We're also using different Stable Diffusion models, due to the choice of software projects. Nod.ai's Shark version uses SD2.1, while Automatic 1111 and OpenVINO use SD1.4 (though it's possible to enable SD2.1 on Automatic 1111). Again, if you have some inside knowledge of Stable Diffusion and want to recommend different open source projects that may run better than what we used, let us know in the comments (or just [email Jarred](mailto:jarred.walton@futurenet.com)).

Image 1 of 11

![Stable Diffusion sample images](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

![Stable Diffusion sample images](https://www.tomshardware.com/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

Our testing parameters are the same for all GPUs, though there's no option for a negative prompt option on the Intel version (at least, not that we could find). The above gallery was generated using Automatic 1111's webui on Nvidia GPUs, with higher resolution outputs (that take much, _much_ longer to complete). It's the same prompts but targeting 2048x1152 instead of the 512x512 we used for our benchmarks. Note that the settings we chose were selected to work on all three SD projects; some options that can improve throughput are only available on Automatic 1111's build, but more on that later. Here are the pertinent settings:  
  
**Positive Prompt:  
**postapocalyptic steampunk city, exploration, cinematic, realistic, hyper detailed, photorealistic maximum detail, volumetric light, (((focus))), wide-angle, (((brightly lit))), (((vegetation))), lightning, vines, destruction, devastation, wartorn, ruins  
  
**Negative Prompt:  
**(((blurry))), ((foggy)), (((dark))), ((monochrome)), sun, (((depth of field)))  
  
**Steps:  
**100  
  
**Classifier Free Guidance:**  
15.0  
  
**Sampling Algorithm:  
**Some Euler variant (Ancestral on Automatic 1111, Shark Euler Discrete on AMD)  
  
The sampling algorithm doesn't appear to majorly affect performance, though it can affect the output. Automatic 1111 provides the most options, while the Intel OpenVINO build doesn't give you any choice.  
  
Here are the results from our testing of the AMD RX 7000/6000-series, Nvidia RTX 40/30-series, and Intel Arc A-series GPUs. Note that each Nvidia GPU has two results, one using the default computational model (slower and in black) and a second using the [faster "xformers" library from Facebook](https://github.com/facebookresearch/xformers) (faster and in green).

[Sponsored Links](https://popup.taboola.com/en/?template=colorbox&utm_source=futureplc-tomshardwarecom&utm_medium=referral&utm_content=thumbnails-a-mid:Mid Article:)

[

](https://taongafarm.com/de/landings/gp/28 "Das entspannendste Spiel des Jahres 2022. Ohne Installation")[Das entspannendste Spiel des Jahres 2022. Ohne InstallationTaonga: Die Inselfarm](https://taongafarm.com/de/landings/gp/28 "Das entspannendste Spiel des Jahres 2022. Ohne Installation")[](https://trc.taboola.com/futureplc-tomshardwarecom/log/3/click?pi=%2Fnews%2Fstable-diffusion-gpu-benchmarks&ri=dc166a7d5f8f2714985db794aedc1bcc&sd=v2_36979fd158ba298466ae9b4a7e34eb87_66a4ec10-5948-4981-9164-9576b5bd72f7-tuctb96c123_1688026019_1688026019_CAwQy-9IGLPtw7GQMSABKAEwODib4wlAjYoQSK6z2QNQ____________AVgAYABo_LuwyLKmzYe-AXAB&ui=66a4ec10-5948-4981-9164-9576b5bd72f7-tuctb96c123&it=text&ii=~~V1~~3628447346035153166~~BKoGCWTlUnf4gNgu1jjiAnqd-dUV76UJSp5oiwy_ZFL6nH0OabNJtzzP-ddPU2nvK8Bm7FKD2NW1M1BCiW1-kuMDMqg65-jJbi04eURsbtqeHe1S9jo_X4timp5pCZhQQas41f4COFvufOf52grWNe487k0pvO_9ezrwRupEiSMB7CKWDYR-vkpxcdUUzOgEqMBBvkdfag99mRDkZdH7GZIABZnE6iw0vZgovqPMyoCY6eD5jnG1QLwcl4nkEOHw5CoWLlX1uzG9gUBqYmKqk08KJRZ9mwaEcwcGgiTaJHWsUaZak2AcDXKoRwoERbO2SJxwhdJv3jKN701ohCgWIPvdAwBc-tgcz2_jjECScpI4w8PM6vv5gTX6XQUWwWKIP5ZnGm2FEG-o7XA_myzMADLnKYHyDCL2jFSRhl8Cex1yRhLST0Ofez4M8LqX_lrG3LzC3rPZAhWkOGz7RcDUQziWpaA6y5TNJSgSGVkT63tJ3Vjc3de0zIhoJSH_1k7BAHwxDkPBKvC6MFrH1rJZRg&pt=text&li=rbox-t2m&sig=02f596c08f652300481cd99f5067379ad48b113c638c&redir=https%3A%2F%2Ftaongafarm.com%2Fde%2Flandings%2Fgp%2F28%3Fref%3DW_150722_WW_Click_Video_DE%26scr%3Dtaboola%26utm_source%3Dtaboola%26mng%3DVK%26%D1%81%D1%81%3D19917578%26ac%3D3595522699%26pn%3Dfutureplc-tomshardwarecom%26pc%3D1193931%26lpc%3Dgp26%26utm_term%3D1193931_futureplc-tomshardwarecom%26utm_medium%3Ddisplay%26utm_campaign%3DW_150722_WW_Click_Video_DE%26utm_content%3D3595522699%23tblciGiBLUb-MxAHYHsvdMqtSitve-ulNvchtwcni7McGees5dyDJpEcorvnh-KPd1eZj&vi=1688026019507&p=volkagames-taongaww-sc&r=48&lti=em-in-body-sticky_var&ppb=CAc&cpb=Em8yMDIzMDYxOC0yNF9iMi1QUi01Nzk1NC1ERVYtMTM1Mjc3LWVtLWRpc3BsYXktdHJ5LXRvLWltcGxlbWVudC1vbmUtb2YtdGhlLXN1Z2dlc3RlZC1zb2x1dGlvbnMtZml4ZWQtZDZhMzVjMDc1OWIYkuenuQQgnP__________ASoZYW0udGFib29sYXN5bmRpY2F0aW9uLmNvbTIIdHJjNDAyODQ4gObPrg1Am-MJSI2KEFCus9kDWP___________wFjCPtGEOVdGDBkYwjd__________8BEN3__________wEYI2RjCIgqEKc4GCRkYwjSAxDgBhgIZGMIlhQQmhwYGGRjCIMvEJNGGAlkYwjIRhCeXRgKZGMI6yQQgDIYHWRjCPQUEJ4dGB9kYwjR__________8BENH__________wEYL2R4AYABAogBzsORW5ABHJgBje7DsZAx&cta=true)

![Stable Diffusion initial benchmarks, January 2023](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

As expected, Nvidia's GPUs deliver superior performance — sometimes by massive margins — compared to anything from AMD or Intel. With the DLL fix for Torch in place, the RTX 4090 delivers 50% more performance than the RTX 3090 Ti with xformers, and 43% better performance without xformers. It takes just over three seconds to generate each image, and even the RTX 4070 Ti is able to squeak past the 3090 Ti (but not if you disable xformers).  
  
Things fall off in a pretty consistent fashion from the top cards for Nvidia GPUs, from the 3090 down to the 3050. Meanwhile, AMD's RX 7900 XTX ties the RTX 3090 Ti (after additional retesting) while the RX 7900 XT ties the RTX 3080 Ti. The 7900 cards look quite good, while every RTX 30-series card ends up beating AMD's RX 6000-series parts (for now). Finally, the Intel Arc GPUs come in nearly last, with only the A770 managing to outpace the RX 6600. Let's talk a bit more about the discrepancies.  
  
Proper optimizations could double the performance on the RX 6000-series cards. Nod.ai says it should have tuned models for RDNA 2 in the coming days, at which point the overall standing should start to correlate better with the theoretical performance. Speaking of Nod.ai, we also did some testing of some Nvidia GPUs using that project, and with the Vulkan models the Nvidia cards were substantially slower than with Automatic 1111's build (15.52 it/s on the 4090, 13.31 on the 4080, 11.41 on the 3090 Ti, and 10.76 on the 3090 — we couldn't test the other cards as they need to be enabled first).  
  
Based on the performance of the 7900 cards using tuned models, we're also curious about the Nvidia cards and how much they're able to benefit from their Tensor cores. On paper, the 4090 has over five times the performance of the RX 7900 XTX — and 2.7 times the performance even if we discount scarcity. In practice, the 4090 right now is only about 50% faster than the XTX with the versions we used (and that drops to just 13% if we omit the lower accuracy xformers result). That same logic also applies to Intel's Arc cards.  
  
Intel's Arc GPUs currently deliver very disappointing results, especially since they support FP16 XMX (matrix) operations that should deliver up to 4X the throughput as regular FP32 computations. We suspect the current Stable Diffusion OpenVINO project that we used also leaves a lot of room for improvement. Incidentally, if you want to try and run SD on an Arc GPU, note that you have to edit the 'stable_diffusion_engine.py' file and change "CPU" to "GPU" — otherwise it won't use the graphics cards for the calculations and takes substantially longer.  
  
Overall then, using the specified versions, Nvidia's RTX 40-series cards are the fastest choice, followed by the 7900 cards, and then the RTX 30-series GPUs. The RX 6000-series underperforms, and Arc GPUs look generally poor. Things could change radically with updated software, and given the popularity of AI we expect it's only a matter of time before we see better tuning (or find the right project that's already tuned to deliver better performance).

RECOMMENDED VIDEOS FOR YOU...

![Stable Diffusion initial benchmarks, January 2023](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

We also ran some tests on legacy GPUs, specifically Nvidia's Turing architecture (RTX 20- and GTX 16-series) and AMD's RX 5000-series. The RX 5600 XT failed so we left off with testing at the RX 5700, and the GTX 1660 Super was slow enough that we felt no need to do any further testing of lower tier parts. But the results here are quite interesting.  
  
First, the RTX 2080 Ti ends up outperforming the RTX 3070 Ti. That doesn't normally happen, and in games even the vanilla 3070 tends to beat the former champion. More importantly, these numbers suggest that Nvidia's "sparsity" optimizations in the Ampere architecture aren't being used at all — or perhaps they're simply not applicable.  
  
We'll get to some other theoretical computational performance numbers in a moment, but again consider the RTX 2080 Ti and RTX 3070 Ti as an example. The 2080 Ti Tensor cores don't support sparsity and have up to 108 TFLOPS of FP16 compute. The RTX 3070 Ti supports sparsity with 174 TFLOPS of FP16, or 87 TFLOPS FP16 without sparsity. The fact that the 2080 Ti beats the 3070 Ti clearly indicates sparsity isn't a factor. The same logic applies to other comparisons like 2060 and 3050, or 2070 Super and 3060 Ti.  
  
As for AMD's RDNA cards, the RX 5700 XT and 5700, there's a wide gap in performance. The 5700 XT lands just ahead of the 6650 XT, but the 5700 lands below the 6600. On paper, the XT card should be up to 22% faster. In our testing, however, it's 37% faster. Either way, neither of the older Navi 10 GPUs are particularly performant in our initial Stable Diffusion benchmarks.  
  
Finally, the GTX 1660 Super on paper should be about 1/5 the theoretical performance of the RTX 2060, using Tensor cores on the latter. If we use shader performance with FP16 (Turing has double the throughput on FP16 shader code), the gap narrows to just a 22% deficit. But in our testing, the GTX 1660 Super is only about 1/10 the speed of the RTX 2060.  
  
Again, it's not clear exactly how optimized any of these projects are. It's also not clear if these projects are fully leveraging things like Nvidia's Tensor cores or Intel's XMX cores. As such, we thought it would be interesting to look at the maximum theoretical performance (TFLOPS) from the various GPUs. The following chart shows the theoretical FP16 performance for each GPU (only looking at the more recent graphics cards), using tensor/matrix cores where applicable. Nvidia's results also include scarcity — basically the ability to skip multiplications by 0 for up to half the cells in a matrix, which is supposedly a pretty frequent occurrence with deep learning workloads.

![Stable Diffusion initial benchmarks, January 2023](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

Those Tensor cores on Nvidia clearly pack a punch (the grey/black bars are without sparsity), and obviously our Stable Diffusion testing doesn't match up exactly with these figures — not even close. For example, on paper the RTX 4090 (using FP16) is up to 106% faster than the RTX 3090 Ti, while in our tests it was 43% faster without xformers, and 50% faster with xformers. Note also that we're assuming the Stable Diffusion project we used (Automatic 1111) doesn't leverage the new FP8 instructions on Ada Lovelace GPUs, which could potentially double the performance on RTX 40-series again.  
  
Meanwhile, look at the Arc GPUs. Their matrix cores should provide similar performance to the RTX 3060 Ti and RX 7900 XTX, give or take, with the A380 down around the RX 6800. In practice, Arc GPUs are nowhere near those marks. The fastest A770 GPUs land between the RX 6600 and RX 6600 XT, the A750 falls just behind the RX 6600, and the A380 is about one fourth the speed of the A750. So they're all about a quarter of the expected performance, which would make sense if the XMX cores aren't being used.  
  
The internal ratios on Arc do look about right, though. Theoretical compute performance on the A380 is about one-fourth the A750, and that's where it lands in terms of Stable Diffusion performance right now. Most likely, the Arc GPUs are using shaders for the computations, in full precision FP32 mode, and missing out on some additional optimizations.  
  
The other thing to notice is that theoretical compute on AMD's RX 7900 XTX/XT improved a lot compared to the RX 6000-series. We'll have to see if the tuned 6000-series models closes the gaps, as Nod.ai said it expects about a 2X improvement in performance on RDNA 2. Memory bandwidth wasn't a critical factor, at least for the 512x512 target resolution we used — the 3080 10GB and 12GB models land relatively close together.

![Stable Diffusion initial benchmarks, January 2023](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

Here's a different look at theoretical FP16 performance, this time focusing only on what the various GPUs can do via shader computations. Nvidia's Ampere and Ada architectures run FP16 at the same speed as FP32, as the assumption is FP16 can be coded to use the Tensor cores. AMD and Intel GPUs in contrast have double performance on FP16 shader calculations compared to FP32.  
  
Clearly, this second look at FP16 compute doesn't match our actual performance any better than the chart with Tensor and Matrix cores, but perhaps there's additional complexity in setting up the matrix calculations and so full performance requires... something extra. Which brings us to one last chart.

![Stable Diffusion initial benchmarks, January 2023](https://vanilla.futurecdn.net/tomshardware/media/img/missing-image.svg)

(Image credit: Tom's Hardware)

This final chart shows the results of our higher resolution testing. We didn't test the new AMD GPUs, as we had to use Linux on the AMD RX 6000-series cards, and apparently the RX 7000-series needs a newer Linux kernel and we couldn't get it working. But check out the RTX 40-series results, with the Torch DLLs replaced.  
  
The RTX 4090 is now 72% faster than the 3090 Ti without xformers, and a whopping 134% faster with xformers. The 4080 also beats the 3090 Ti by 55%/18% with/without xformers. The 4070 Ti interestingly was 22% slower than the 3090 Ti without xformers, but 20% faster with xformers.  
  
It looks like the more complex target resolution of 2048x1152 starts to take better advantage of the potential compute resources, and perhaps the longer run times mean the Tensor cores can fully flex their muscle.  
  
Ultimately, this is at best a snapshot in time of Stable Diffusion performance. We're seeing frequent project updates, support for different training libraries, and more. We'll see about revisiting this topic more in the coming year, hopefully with better optimized code for all the various GPUs.
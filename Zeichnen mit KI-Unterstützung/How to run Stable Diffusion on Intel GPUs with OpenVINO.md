---
source: https://medium.com/openvino-toolkit/how-to-run-stable-diffusion-on-intel-gpus-with-openvino-840714f122b4
---
Note: It works on CPUs too! :)

OpenVINO Notebooks comes with a handful of AI examples. But do you know that we can also run Stable Diffusion and convert the model to OpenVINO Intermediate Representation (IR) Format, and so it can run on CPUs and GPUs efficiently? Also, by compressing the FP32 model to FP16, we reduced the model size by half (close to), and also now it requires much less RAM/VRAM to run. Most importantly, this also provides a significant speed-up in GPU processing because Intel Xe Matrix Extensions (XMX-[**systolic array**](https://www.anandtech.com/show/16895/a-sneak-peek-at-intels-xe-hpg-gpu-architecture)**)** kicked in.

Here are some results I got running the notebook and it’s pretty fun. With my Intel Arc A770m, I can get approximately 6.0 iterations per second (without debug mode). What it means is usually it takes less about 10 seconds to generate a high-quality image below.

![](https://miro.medium.com/v2/resize:fit:640/0*HiR9r22VhKpBt6cn.png)

![](https://miro.medium.com/v2/resize:fit:640/1*QNrePgfZulhAZZqw3Djgaw.png)

![](https://miro.medium.com/v2/resize:fit:640/1*srI15ufZ5I8EwW79B_qdeg.png)

Stable Diffusion text-to-image results with the OpenVINO Notebooks and Intel Arc A770m.

![](https://miro.medium.com/v2/resize:fit:1000/1*a-pwI6bZTzC1QaEMCPvfMA.jpeg)

![](https://miro.medium.com/v2/resize:fit:1000/1*3jZ48S9KcS51G-BJNVM2fQ.png)

Image-to-Image example, turning a photo into a watercolor painting.

First, here is the OpenVINO Notebooks repository. It has everything you would need to complete the demo here today.

openvino_notebooks/notebooks at main · openvinotoolkit/openvino_notebooks

If you wish to launch only one notebook, like the Monodepth notebook, run the command below. In your browser, select a…

github.com
https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks

![](https://miro.medium.com/v2/resize:fit:875/1*UZmi8SX5up3XSvTk6eUU_w.png)

Stable Diffusion is under the 225-stable-diffusion-text-to-image folder

And in the demo notebook, we introduced not only the famous Text-to-mage pipeline but also included the Image-to-Image generation pipeline. But what does it really mean and how do we run it?

![](https://miro.medium.com/v2/resize:fit:875/0*6BUVX1cGrWY0gw1l.png)

Pipelines

## How to Install

Quick Video Instruction.

To install OpenVINO Notebooks, you can follow the instruction here if you are using Windows: [https://github.com/openvinotoolkit/openvino_notebooks/wiki/Windows](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Windows)

If you are a Linux user, you can follow this link: [https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu)

On a high level, it’s a few steps below.

Install Python ==3.10.x==. (or below) and create a virtual environment

```sh
scoop bucket add versions
scoop install versions/python310

```


Git Clone the directory


```sh
git clone --depth=1 https://github.com/openvinotoolkit/openvino_notebooks.git  
cd openvino_notebooks
```

virtual Environment

```sh
python -m venv venv  
. venv/Scripts/Activate.ps1
```

Install all libraries and dependencies

```sh
pip install -r requirements.txt
```


Run the Jupyter Notebooks


```
jupyter lab notebooks

```

![](https://miro.medium.com/v2/resize:fit:875/1*e_azjYzgWPh6N1uPNzOqCg.png)

Run All Cells and wait =)

Now, if you look into the code. What we have done is really optimize the PyTorch pipeline and execute the code with OpenVINO.

![](https://miro.medium.com/v2/resize:fit:875/1*2ilaf0qE3C0-J6MvV-0ACw.png)

The downloading and converting may take a little while for the first time. Once it’s completed you will get a set of IR files. For your convenience, I’ve already updated these pre-trained, optimized models here to huggingface.

![](https://miro.medium.com/v2/resize:fit:875/1*yyn7IuflE7c-K6SbZRWgbw.png)

[

## bes-dev/stable-diffusion-v1-4-openvino at main

### We're on a journey to advance and democratize artificial intelligence through open source and open science.

huggingface.co



](https://huggingface.co/bes-dev/stable-diffusion-v1-4-openvino/tree/main)

Now, if you are blessed with the Intel Arc GPUs, you can change the code to “GPU”. By default, it’s using AUTO, and thus it will switch to GPU automatically if it’s detected.

![](https://miro.medium.com/v2/resize:fit:875/1*n783B-qYMJ-dt8UK1an9ew.png)

Make it run on GPUs

![](https://miro.medium.com/v2/resize:fit:875/1*vFs3nXXqDs6qqbtNJpEAaw.png)

Auto-plugin. It started by first using the CPU, then switch to GPU automatically.

And here in this step, I have set the steps to 30. Ideally, I would use 50 as it will provide the best-looking results. You can generate different scenes here by modifying the input text. If you want to get some really cool looking images, you can try some of the top prompts the community put together. [https://mpost.io/best-100-stable-diffusion-prompts-the-most-beautiful-ai-text-to-image-prompts/](https://mpost.io/best-100-stable-diffusion-prompts-the-most-beautiful-ai-text-to-image-prompts/)

![](https://miro.medium.com/v2/resize:fit:875/1*gYVJGyXqoLZ106gvcIU3Vg.png)

In the end, we also generated the GIF file for you to visualize what happened between each step.

![](https://miro.medium.com/v2/resize:fit:4800/1*p3K8TN09UsWYgL69ifi_hQ.png)

![](https://miro.medium.com/v2/resize:fit:640/1*P_FaedcSm0T0Rx-WFw9GDg.gif)

## Image-to-image pipeline

Now, if you continue on the notebooks, you will see we can also use a prompt to ‘influence’ the look of the final image. Here we provided an example of converting our photo into a watercolor painting.

![](https://miro.medium.com/v2/resize:fit:4800/1*jqhz7YbaENVeiEgJfoTfqQ.png)

![](https://miro.medium.com/v2/resize:fit:1650/1*rrmvwzNB6EHm_-KBOTGR_A.gif)

Generating an image based on an initial image and a prompt. This way the result will be guided.

![](https://miro.medium.com/v2/resize:fit:1650/1*vtvsYVcgDKIi77ApmmgZ7g.jpeg)

![](https://miro.medium.com/v2/resize:fit:1650/1*TbjMIz7MDZbJy2O08hTYAA.png)

Image-to-image result.

**UPDATE:** Stable Diffusion v2 is now available on OpenVINO Notebooks too.

[

## openvino_notebooks/notebooks/236-stable-diffusion-v2 at main · openvinotoolkit/openvino_notebooks

### Stable Diffusion v2 is the next generation of Stable Diffusion model a text-to-image latent diffusion model created by…

github.com



](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/236-stable-diffusion-v2)

## Conclusion

Today, if you want to learn how Stable Diffusion works and also see how hardware acceleration works with Intel hardware, the OpenVINO Notebooks is definitely my go-to. If you have any questions or want to show some of your best results, please make a comment here or on our GitHub discussion board! Happy coding.
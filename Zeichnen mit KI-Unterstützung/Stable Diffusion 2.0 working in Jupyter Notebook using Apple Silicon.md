---
source: https://spcman.github.io/stable-diffusion-m1/stable-diffusion-2-jupyter-apple-mac-silicon/
---
Stable Diffusion 2 (SD2) has been released and the diffusers library already supports it. The HuggingFace upgrade has support for 768x768 higher resolution imagery and built in image upscaling. I also read [this article](https://appleinsider.com/articles/22/12/01/new-betas-have-apple-silicon-optimizations-for-stable-diffusion-ai-art-generator) today about stable diffusion support within the Mac operating system which is quite exciting. I upgraded my Mac’s operating system to Ventura 13.1.

Before upgrading to SD2 I backed up and cloned the working stable diffusion 1.x conda environment and started a new one. I had some trouble again with libraries and dependences especially this annoying error: `ImportError: cannot import name 'ReduceOp' from 'torch.distributed.`

Eventually I got it running in the new environment and tested it as per the notebook below. The line `torch.distributed.is_available()` is a check that the problematic pytorch library is available. If you’ve ended up here having the same issue on your Mac, try installing the latest nightly pytorch release and then restart the kernel.

Here is a simple working example in a Jupyter notebook on Apple Silicon.

```
import PIL
import requests
import torch
from io import BytesIO
```

```
torch.distributed.is_available()
```

```
True
```

```
from diffusers import DiffusionPipeline
DEVICE='mps'
pipe = DiffusionPipeline.from_pretrained("stable-diffusion-2-base").to(DEVICE)
```

```
prompt = "a photo of an astronaut riding a horse on mars"
image = pipe(prompt).images[0]
image
```

![stable-diffusion-2](https://spcman.github.io/stable-diffusion-m1/images/005/output_4_0.png)

**Updated:** December 16, 2022
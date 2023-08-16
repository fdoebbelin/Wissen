---
source: https://github.com/AUTOMATIC1111/stable-diffusion-webui
---

A browser interface based on Gradio library for Stable Diffusion.

### Automatic Installation on Windows

1. Install [Python 3.10.6](https://www.python.org/downloads/release/python-3106/) (Newer version of Python does not support torch), checking "Add Python to PATH".
2. Install [git](https://git-scm.com/download/win).
3. Download the stable-diffusion-webui repository, for example by running `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git`.
4. Edit `webui-user.bat` to disable cuda check
   `set COMMANDLINE_ARGS=--skip-torch-cuda-test`
5. Run `webui-user.bat` from Windows Explorer as normal, non-administrator, user.


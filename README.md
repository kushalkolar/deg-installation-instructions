# deg-installation-instructions

Tested on Ubuntu 21.04 with CUDA version 11.4 and nvidia driver 470.86

If you don't know what you're doing just copy paste this entire block into the terminal.

```
# Create a venv
python3 -m venv /share/python-venvs/deg

# Open a new terminal and activate the venv
ae_deg

# ae_deg will work if the /share/.bashrc is present, otherwise do this
# source /share/python-venvs/deg/bin/activate

# upgrade pip etc.
pip install --upgrade pip wheel setuptools

# some pre-reqs
pip install numpy cython

# non-headless opencv gives issues
pip install opencv-python-headless

# install pytorch using this URL
# the helper tool on the website gives a broken URL
# so I had to find it manually ¯\_(ツ)_/¯
pip install https://download.pytorch.org/whl/cu111/torch-1.9.0%2Bcu111-cp39-cp39-linux_x86_64.whl

# install vidio and deepethogram from my fork
# the maintainer hasn't updated the setup.py to use opencv-python-headless
# so the "official" version is broken ¯\_(ツ)_/¯
pip install git+https://github.com/kushalkolar/vidio.git
pip install git+https://github.com/kushalkolar/deepethogram.git
```

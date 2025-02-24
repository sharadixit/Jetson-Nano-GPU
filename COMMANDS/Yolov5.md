# YOLOV5 

## Download PyTorch
### Version : PyTorch v1.10.0
```
# JetPack 4.4 (L4T R32.4.3) / JetPack 4.4.1 (L4T R32.4.4) / JetPack 4.5 (L4T R32.5.0) / JetPack 4.5.1 (L4T R32.5.1) / JetPack 4.6 (L4T R32.6.1)
# Python 3.6 - 
$ torch-1.10.0-cp36-cp36m-linux_aarch64.whl

# This is the final PyTorch release supporting Python 3.6.

```

### Verify PyTorch version
```
python3
$ import torch
$ print(torch.__version__)
```
## Download TorchVision
```
$ sudo apt-get install libjpeg-dev zlib1g-dev libpython3-dev libopenblas-dev libavcodec-dev libavformat-dev libswscale-dev
$ git clone --branch v0.11.1 https://github.com/pytorch/vision torchvision   
# see below for version of torchvision to download
$ cd torchvision
$ export BUILD_VERSION=v0.11.1  
# where 0.x.0 is the torchvision version  
$ python3 setup.py install --user
$ cd ../  
# attempting to load torchvision from build dir will result in import error
$ pip install 'pillow<7' 
# always needed for Python 2.7, not needed torchvision v0.5.0+ with Python 3.6
```
### Verify TorchVision version
```
$ python3
$ import torchvision
$ print(torchvision.__version__)
```
# Another method

## If you face problem in version 
```
$ pip uninstall torchvision -y
$ rm -rf torchvision
$ rm -rf ~/.cache/pip
```

## Again Insatall TorchVision By this method

```
$ wget https://nvidia.box.com/shared/static/9h3a7dlqb5vs5krn20pzy4h9pxz92a6x.whl -O torchvision-0.9.0-cp36-cp36m-linux_aarch64.whl
$ pip install torchvision-0.9.0-cp36-cp36m-linux_aarch64.whl
```

## Setup.py

```
$ git clone --branch v0.9.0 https://github.com/pytorch/vision torchvision
$ cd torchvision
$ python3 setup.py install
```
## Install ultralytics
```
pip install ultralytics
```

## Env creation
```
$ source yolov5_env/bin/activate
```
### Install requirements.txt
```
pip install --upgrade pip
pip install -r requirements.txt
```
## Python have this time 3.8 version
```
$ sudo apt update
$ sudo apt install python3.8 python3.8-venv $ $ python3.8-dev -y
$ sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1
$ sudo update-alternatives --config python3  # Select Python 3.8
```
### Use Yolov5
```
$ cd yolov5
```
## Remove Old Env
```
$ rm -rf yolov5_env  # Remove old environment
$ python3 -m venv yolov5_env
$ source yolov5_env/bin/activate
$ pip install --upgrade pip
```
# TEST DATA 
```
# FOR IMAGES
$ python detect.py --source ../test_img.jpg --weights yolov5s.pt 
# FOR MP4
$ python detect.py --source ../test.mp4 --weights yolov5s.pt 
# FOR USB CAMERA
$ python detect.py --source ../0 --weights yolov5s.pt 

```

# YOLOV8

## COMMANDS
```
$ cd ~
# FOR IMAGES
$ yolo task=detect mode=predict model=yolov8n.pt source=your_image.jpg
# FOR USB CAMERA
$ yolo task=detect mode=predict model=yolov8n.pt source=0
```


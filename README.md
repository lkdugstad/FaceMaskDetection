# FaceMaskDetection


## Setup the RaspberryPi
Use a RPI4b and the RPI Camera<br/>
Download the Raspberry Pi Imager: https://www.raspberrypi.org/software/<br/>
Install the Raspberry PI OS  (32-bit) version<br/>
Mount the Camera Module: https://projects.raspberrypi.org/en/projects/getting-started-with-picamera

## Install a virtual Environment      
1. Open Terminal / BASH
2. Create a folder for your project
```bash
mkdir environment
```
3. Navigate to the project folder
```bash
cd environment
```
4. Create the virtual environment 
```bash
python3 -m venv ./venv
```
5. Activate the virtual environment
```bash
source ./venv/bin/activate
```
## Install Tensorflow
```bash
sudo apt-get install -y libhdf5-dev libc-ares-dev libeigen3-dev
python3 -m pip install keras_applications==1.0.8 --no-deps
python3 -m pip install keras_preprocessing==1.1.0 --no-deps
python3 -m pip install h5py==2.9.0
sudo apt-get install -y openmpi-bin libopenmpi-dev
sudo apt-get install -y libatlas-base-dev
python3 -m pip install -U six wheel mock
```
pick a tensorflow version from: https://github.com/lhelontra/tensorflow-on-arm/releases
```bash
wget https://github.com/lhelontra/tensorflow-on-arm/releases/download/v2.3.0/tensorflow-2.3.0-cp37-none-linux_armv7l.whl```
python3 -m pip uninstall tensorflow
python3 -m pip install tensorflow-2.3.0-cp37-none-linux_armv7l.whl
```
## Install Open Computer Vision
```bash
python3 -m pip install opencv-python
```
Restart your Terminal or bash
Reactivate Virtual Environment
```bash
cd environment
source ./venv/bin/activate
```
## Start the video Stream
```bash
python3 videoStream.py
```
close the videoStream with ESC


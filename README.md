# Panda3D-Raspbian
Version of Panda3D compiled for Raspbian Buster

Steps used to compile:

Installed all dependencies, then started compile script: 

sudo apt update
sudo apt-get install libvorbis-dev libeigen3-dev libopenal-dev libode-dev libbullet-dev  libgtk2.0-dev libassimp-dev libopenexr-dev -y
sudo apt-get install  libxrandr-dev libxxf86dga-dev libxcursor-dev bison flex libfreetype6-dev-y
sudo apt-get install build-essential pkg-config fakeroot python-dev libpng-dev libjpeg-dev libtiff-dev zlib1g-dev libssl-dev libx11-dev -y  sudo apt install libgl1-mesa-dev libxrandr-dev libxxf86dga-dev libxcursor-dev bison flex libfreetype6-dev -y
git clone https://github.com/panda3d/panda3d.git && cd panda3d
python makepanda/makepanda.py --everything --installer --no-egl --no-gles --no-gles2 --no-opencv


Compiling took about 3 hours and resulted in the .deb file, which used Python 3.5.3 and Raspberry Pi's ARM architecture. 

Installing Panda3d was as simple as running dpkg: sudo dpkg -i panda3d1.11_1.11.0_armhf.deb


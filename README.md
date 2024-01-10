# QUADRUPED ROBOT -- UNFINISHED
Work-in-progress Quadruped Robot

## January 2nd, 2024:

Have you ever wanted to build a robotic dog? Ight bet. This repo acts as a log and build guide for it.

![robot render 1](https://github.com/nicckko/quadruped-dog/assets/109701332/6ae72708-bed5-4252-bbf3-ab66df5ebeb8)

![robot render 3](https://github.com/nicckko/quadruped-dog/assets/109701332/3b947949-547d-4c1e-ae6e-3f22a45aac66)

### Preparing the operation system

To run the servos and machine learning of the robot, an 8gb Raspberry Pi 5 will be used with Docker and Kubernetes. First, the operating system needs to be prepared. Install the most recent version of Ubuntu Server for the Raspberry Pi that you are using. Make sure to enable ssh. When that is done, plug in the SD card to your Pi and wait for it to boot. From there, follow this code:

``` bash
sudo su -


sudo apt-get update

sudo apt-get install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev;
wget https://www.python.org/ftp/python/3.10.0/Python-3.10.0.tgz;
tar -xf Python-3.10.0.tgz;
cd Python-3.10.0;
./configure --enable-optimizations;

make -j$(nproc);
sudo make altinstall;

cd

sudo su (USER)

sudo apt install -y gcc g++ make python3-dev python3-pip python3-pyqt6;
python3.10 -m pip install pylx16a;
```

Once that is done, you should have a working install of Ubuntu Linux with Python 3.10 and PyLX16A installed. PyLX16A is the updated Python module/library to control the LX16A servos. Docker and Kubernetes will be installed after the robot is fully assembled and working as it is only necessary for machine learning and using more than one Pi.

ERROR WHEN DOING PYTHON3.10 -M PIP INSTALL PYLX16A NEVER INSTALLED !!

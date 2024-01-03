# QUADRUPED ROBOT
Work-in-progress Quadruped Robot

## January 2nd, 2024:

Since I could remember, I have always wanted my dog to have another dog to play with. I realized that if I could not force my parents to buy one, why couldn't I just make one? This repo serves as not just my files for my robot, but also as a log as I continue to work on this robot. As of today, I have built a working leg prototype, yet the code is not there yet...

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

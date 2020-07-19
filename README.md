Welcome to OpenRAVE
-------------------

# Installation for ubuntu 18.04:
```
sudo apt install git
sudo apt install libboost-filesystem-dev libboost-system-dev libboost-python-dev libboost-thread-dev libboost-iostreams-dev libboost-numpy-dev
sudo apt install libqt4-dev qt4-dev-tools libxml2-dev libode-dev
sudo apt install libsoqt4-dev libcoin80-dev
sudo apt install rapidjson-dev liblapack-dev
sudo apt install python-scipy  # For openravepy. Note that Xenial sympy is 0.7.6, see next line
pip install --upgrade --user sympy==0.7.1 # OpenRAVE ikfast needs sympy 0.7.1, https://github.com/rdiankov/openrave/pull/407
sudo apt install libcollada-dom2.4-dp-dev  # Open .zae files, only Ubuntu 16.04
cd  # go home
mkdir -p repos; cd repos  # create $HOME/repos if it doesn't exist; then, enter it
git clone --branch boost-1.6x-forcompile https://github.com/roboticslab-uc3m/openrave.git # git clone --branch master https://github.com/rdiankov/openrave.git
cd openrave; mkdir build; cd build
cmake .. -DOPT_VIDEORECORDING=OFF  # Avoids AV errors
make -j$(nproc)
sudo make install; cd  # install and go home
```

This project is an early stage prototype of unix AirPlay server.
Work is based on https://github.com/FD-/RPiPlay.
Tested on Ubuntu 19.10 desktop.
5G Wifi connection is the must.

Features:
1. Based on Gstreamer.
1. Video and audio are supported out of the box.
3. Gstreamer decoding is plugin agnostic. Uses accelerated decoders if availible. VAAPI is preferable.
4. Automatic screen orientation.

Building:
1. sudo apt-get install cmake
2. sudo apt-get install libssl-dev libavahi-compat-libdnssd-dev libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev gstreamer1.0-libav
3. sudo apt-get install gstreamer1.0-vaapi (For Intel graphics)
4. mkdir build
5. cd build
6. cmake ..
7. make

Building on Fedora:
1. sudo dnf install cmake gcc gcc-c++ openssl-devel avahi-compat-libdns_sd-devel gstreamer1-devel gstreamer1-plugins-base-devel gstreamer1-libav gstreamer1-vaapi
2. mkdir build
3. cd build 
4. cmake ..
5. make
6. sudo systemctl stop firewalld

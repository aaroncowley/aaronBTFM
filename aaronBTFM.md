# Aaron Cowley's Blue Team Field Manual

## Tools
This section covers quick installation and usage guides for my favorite tools
### Bro/Zeek
#### Installation from source
Dependencies:
+ RPM/Redhat Linux
```bash
sudo yum install cmake make gcc gcc-c++ flex bison libpcap-devel openssl-devel python-devel swig zlib-devel curl
```
+ APT/Debain Linux
```bash
sudo apt-get install cmake make gcc g++ flex bison libpcap-dev libssl-dev python-dev swig zlib1g-dev curl
```

Install:
```bash
git clone --recursive https://github.com/zeek/zeek && cd zeek
./configure
make
sudo make install
```
Add zeek to path:
```bash
export PATH=/usr/local/zeek/bin:$PATH
```

Basic Usage:
+ set the interface in node.cfg
```bash
vim /usr/local/zeek/etc/node.cfg
```
+ Comment out defaults and add network for zeek to monitor
```bash
vim /usr/local/zeek/etc/networks.cfg
```
+ change mailto to whoever you want and set log rotation interval
```bash
vim /usr/local/zeek/etc/zeekctl.cfg
```
## Your Hiveos must be in Beta version (6.1)

Best way to update hiveos : 
```sh
hive-replace -y --beta
```

## Update your system :

```sh
selfupgrade
```
```sh
apt update && apt install unzip g++ gcc  -y
```

## Install Zluda :
```sh
mkdir /usr/lib/zluda && cd /usr/lib/zluda && wget https://github.com/Gddrig/Qubic-AMD/releases/download/3.22/zluda_hiveos-6.1.zip && unzip zluda_hiveos-6.1.zip && chmod +rwx /usr/lib/zluda/* && cd /
```

## Update ROCM 5.7 for Hiveos :
```sh
amd-ocl-install 5.7 5.7
```

## Install the library necessary for Zluda to work with Rocm :
```sh
cd /opt/rocm/lib && wget https://github.com/Gddrig/Qubic-AMD/releases/download/3.22/libamdhip64.so.zip && unzip libamdhip64.so.zip && chmod +rwx /opt/rocm/lib/* && rm libamdhip64.so.zip && cd / && ldconfig
```


## Possible issue

**You have lib errors**

**First, install glibc/lib6, and retry :**
```sh
apt update && echo "deb http://cz.archive.ubuntu.com/ubuntu jammy main" >> /etc/apt/sources.list && apt update && apt install tmux -y && apt install libc6 -y
```

**If you still have an error install glibcxx :**
```sh
apt install g++-11
```

## Flightsheet example :

![alt text](https://github.com/Gddrig/Qubic_Hiveos/blob/main/Capture.PNG)

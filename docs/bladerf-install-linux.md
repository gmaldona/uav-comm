# BladeRF Lib Install / BladeRF Sink for GNURadio (Debian Linux)

## Install BladeRF Lib
https://github.com/Nuand/bladeRF 

Follow the installation docs [here](https://github.com/Nuand/bladeRF/wiki/Getting-Started%3A-Linux).

To check if the installation was successful, the BladeRF CLI tools should be
in your shell path.

```shell
$ bladeRF-cli --version
% 1.9.0-git-b40cd829
```

## Install Soapy
https://github.com/pothosware/SoapySDR

Follow the installation docs [here](https://github.com/pothosware/SoapySDR/wiki#installation).

## Install BladeRF Soapy Plugin
https://github.com/pothosware/SoapyBladeRF

```shell
git clone https://github.com/pothosware/SoapyBladeRF ./SoapyBladeRF
cd SoapyBladeRF
mkdir build && cd build
cmake .. 
make
make install
```
# BladeRF Lib Install / BladeRF Sink for GNURadio (Debian Linux)

Note as of 2024-06-12: BladeRF lib / soapySDR / soapySDR BladeRF seems to come pre-installed
when downloading GNURadio using a package manager. 

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

## BladeRF Troubleshooting

### [WARNING @ host/libraries/libbladeRF/src/board/bladerf2/bladerf2.c:461] FPGA bitstream file not found.

* READ FOR THE SOLUTION: https://nuand.com/forums/viewtopic.php?t=3841
The firmware used as of 2024-06-12 is placed in [here](../firmware/hostedxA4-latest.rbf) or download the latest at [nuand.com](https://www.nuand.com/fpga_images/).

* Flash the fireware to the board: `bladeRF-cli -l path/to/fireware/hostedxA4-latest.rbf` 
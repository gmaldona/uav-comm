# BladeRF Lib Install / BladeRF Sink for GNURadio (MacOS)

don't... install a VM if you have too.

## Prerequisites

* GNURadio (version >= 3.7)
   * https://wiki.gnuradio.org/index.php/MacInstall
* PyBind11
   * brew: `brew install pybind11`

## BladeRF Lib Install

* [Getting Started MacOSX](https://github.com/Nuand/bladeRF/wiki/Getting-started%3A-Mac-OSX)

* `git clone https://github.com/Nuand/bladeRF.git && cd bladeRF`
* `cd host && mkdir build && cd build`
* `cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr/local`
   * Add `/usr/local/bin` to your shell PATH e.g. `PATH=$PATH:/usr/local/bin`
* To confirm, in a new shell, execute:

```shell
$ bladeRF-cli --version

% 1.9.0-git-b40cd829
```

## Plugin for Popular SDR to Use to GNURadio (GR-OSMOSDR)
https://github.com/Nuand/gr-osmosdr

* `git clone https://github.com/Nuand/gr-osmosdr.git && cd gr-osmosdr`
* `mkdir build && cd build` 
* `cmake ../ && sudo make install`

CMake logs should output nuad bladeRF support enabled:
```
-- Configuring nuand bladeRF support...
--   Dependency LIBBLADERF_FOUND = TRUE
--   Enabling nuand bladeRF support.
--   Override with -DENABLE_BLADERF=ON/OFF
```

## Troubleshooting as of 2024-06-11

### Using brew to install GNURadio (grrrr.....)
* PyBind11 did not install when I downloaded GNURadio using brew. Using pip3 to install PyBind11 also 
did not work. A quick solution was to use `brew install pybind11`. 
   * Probably can find a setting/flag to know which dir to search through but brew worked just fine.
* Python package `six` did not install when downloading GNU using brew. Using pip3 to install six also
did not work. A quick solution was to use `brew install six`.
   * Where the packages get installed for brew is different for where pip uses. Probably can
   consolidate the two but this is a QUICK (as possible) START. 




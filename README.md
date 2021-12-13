# [wb32-dfu-updater_cli](https://github.com/WestberryTech/wb32-dfu-updater)

`wb32-dfu-updater` is a host tool used to download and upload firmware to/from WB32 MCU via USB. (`wb32-dfu-updater_cli` is the command line version)

## How to build wb32-dfu-updater_cli on MacOs / Linux:

The following operations depend on [Homebrew](https://docs.brew.sh/Installation) and [CMake](https://gitlab.kitware.com/cmake/community/-/wikis/home), please ensure that they are installed on your system.

### 1. Install the [libusb](https://libusb.info/) library.

- ``` brew install libusb ```
- ``` brew list libusb ```
-  Record the installation path of Libusb 

### 2. Install the wb32-dfu-updater_cli.
- ``` git clone https://github.com/WestberryTech/wb32-dfu-updater.git ```
- ``` cd wb32-dfu-updater ```
- ``` mkdir build ```
- ``` cd build ```
- ``` cmake .. -DCMAKE_BUILD_TYPE=Release -DLIBUSB_INCLUDE_DIRS=[path to libusb]/[libusb version]/include/libusb-1.0 -DLIBUSB_LIBRARIES=[path to libusb]/[libusb version]/lib/libusb-1.0.dylib ```
- ``` make install ``` 

## How to build wb32-dfu-updater_cli on Windows:

The following operations depend on [vcpkg](https://github.com/microsoft/vcpkg) and [CMake](https://gitlab.kitware.com/cmake/community/-/wikis/home), please ensure that they are installed on your system.

### 1. Install the [libusb](https://libusb.info/) library.

- ``` vcpkg install libusb ```

### 2. Install the wb32-dfu-updater_cli.
- ``` git clone https://github.com/WestberryTech/wb32-dfu-updater.git ```
- ``` cd wb32-dfu-updater ```
- ``` mkdir build ```
- ``` cd build ```
- ``` cmake .. -DCMAKE_TOOLCHAIN_FILE="[path to vcpkg]/scripts/buildsystems/vcpkg.cmake" ```
- ``` make install ``` 

## Windows driver

You can found the Windows driver for wb32-dfu-updater_cli in the `windows_driver` directory.

To install the Windows driver for wb32-dfu-updater_cli, you should unzip the package and run `winusb_install.bat`.
## Introduction
This is manifest repository for raspberry pi yocto compilation It will allow repo tool to download all projects required to build the bsp.

### Building RPI3 Yocto Distribution

```python
mkdir -p rpi_yocto_build
repo init -u https://github.com/nullbyte91/Yocto-manifest-RPI -m manifest.xml -b nullbyte_91
repo sync
source sources/poky/oe-init-build-env
```

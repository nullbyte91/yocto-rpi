## Introduction
This is manifest repository for raspberry pi yocto compilation It will allow repo tool to download all projects required to build the bsp.

### Building RPI3 Yocto Distribution

```python
mkdir -p rpi_yocto_build
repo init -u https://github.com/nullbyte91/Yocto-manifest-RPI -m manifest.xml -b nullbyte_91
repo sync
source sources/poky/oe-init-build-env
#Customize the configuration files
cp ../sources/meta-rpi/conf/local.conf.sample conf/local.conf
cp ../sources/meta-rpi/conf/bblayers.conf.sample conf/bblayers.conf
```

```python3
#Build the image
bitbake core-image-minimal
bitbake core-image-sato
bitbake meta-toolchain
bitbake meta-ide-support
```

# OpenCV build script for Tegra

This script builds OpenCV from source on Tegra (Gen Orin(**CUDA_ARCH_BIN=8.7**) ).

Related thread on Nvidia developer forum 
[here](https://devtalk.nvidia.com/default/topic/1051133/jetson-nano/opencv-build-script/).

[How it Works](https://wiki.debian.org/QemuUserEmulation)

## Usage:
```shell
# swiftfile sets default opencv ver to 4.5.5.
./build_opencv.sh
```

## Specifying an OpenCV version (git branch)
```shell
./build_opencv.sh 4.5.5 
```

Where `4.4.0` is any version of openCV from 2.2 to 4.4.0
(any valid OpenCV git branch or tag will also attempt to work, however the very old versions have not been tested to build and may require spript modifications.).

**JetPack 4.4 NOTE:** the minimum version that will build correctly on JetPack 4.4 GA is 4.4.0. Prior versions of JetPack may need the CUDNN version adjusted (the `-D CUDNN_VERSION='8.0'` line can simply be removed).

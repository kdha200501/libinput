# How to

##### Install dependencies

```shell
$ sudo dnf install meson ninja-build
$ sudo dnf install mtdev-devel.x86_64 libevdev-devel.x86_64 libwacom-devel.x86_64 check-devel.x86_64
```



##### Compile and install `libinput`

```shell
$ libinput --version
$ git checkout customize/v<x.y.z>
$ mkdir build
$ meson setup --prefix=/usr build/
$ ninja -C build/ -j$(nproc)
$ sudo ninja -C build/ install
```





# Customization

##### Disable three finger tap


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
$ meson setup --prefix=/usr -Dversion=v<x.y.z> build/ .
$ ninja -C build/ -j$(nproc)
$ sudo ninja -C build/ install
```





# Customization

##### Disable three finger tap

When two finger tap is configured to trigger right click, three finger tap is forcefully configured to trigger middle click. The middle click invokes paste. The three finger tap can only be disabled through recompiling `libinput`

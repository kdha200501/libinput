# How to

##### branch off from the upstream tag corresponding to the latest package version

```shell
$ cd libinput
$ git checkout master
$ ./create-branch.sh
```

##### Sort out dependencies

```shell
$ sudo group install "development-tools"
$ sudo dnf builddep libinput
$ mkdir build
$ meson setup ./build . --prefix=/usr --buildtype=release -Dlibdir=lib64 -Dtests=false -Ddocumentation=false -Ddebug-gui=false
```

##### Compile and install `libinput`

```shell
$ cd build
$ ninja -j"$(nproc)"
$ sudo ninja install
```

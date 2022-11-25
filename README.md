Nuvoton MA35D1 development to use [kas](https://github.com/siemens/kas)
===

#### this branch for kirkstone with OP-TEE v3.18/ARM Trusted Firmware v2.6

use the below command for build 'core-image-minimal' image for [Numaker-IoT-MA35D1-A1](https://www.nuvoton.com/products/iot-solution/iot-platform/numaker-iot-ma35d1-a1/)
```
./kas-container build numarker-iot-ma35d1-a1.yaml
```

run log
```
$ ./kas-container build numarker-iot-ma35d1-a1.yaml
2022-11-25 08:06:12 - INFO     - kas 3.1 started
2022-11-25 08:06:12 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:12 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:12 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:12 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-25 08:06:12 - INFO     - /work/sources/meta-arm$ git remote set-url origin git://git.yoctoproject.org/meta-arm
2022-11-25 08:06:12 - INFO     - /work/sources/meta-virtualization$ git remote set-url origin git://git.yoctoproject.org/meta-virtualization
2022-11-25 08:06:12 - INFO     - /work/sources/meta-qt5$ git remote set-url origin https://github.com/meta-qt5/meta-qt5
2022-11-25 08:06:12 - INFO     - /work/sources/poky$ git remote set-url origin git://git.yoctoproject.org/poky
2022-11-25 08:06:12 - INFO     - /work/sources/meta-openembedded$ git remote set-url origin https://github.com/openembedded/meta-openembedded
2022-11-25 08:06:12 - INFO     - /work/sources/ma35d1-yocto$ git remote set-url origin https://github.com/UWINGS-KUNYI/MA35D1_Yocto.git
2022-11-25 08:06:12 - INFO     - /work/sources/meta-arm$ git cat-file -t kirkstone
2022-11-25 08:06:12 - INFO     - /work/sources/meta-virtualization$ git cat-file -t kirkstone
2022-11-25 08:06:12 - INFO     - /work/sources/meta-qt5$ git cat-file -t kirkstone
2022-11-25 08:06:12 - INFO     - /work/sources/poky$ git cat-file -t kirkstone
2022-11-25 08:06:12 - INFO     - /work/sources/meta-openembedded$ git cat-file -t kirkstone
2022-11-25 08:06:12 - INFO     - /work/sources/ma35d1-yocto$ git cat-file -t kirkstone-v2
2022-11-25 08:06:12 - INFO     - Repository sources/meta-arm already contains kirkstone as commit
2022-11-25 08:06:12 - INFO     - Repository sources/meta-virtualization already contains kirkstone as commit
2022-11-25 08:06:12 - INFO     - Repository sources/meta-qt5 already contains kirkstone as commit
2022-11-25 08:06:12 - INFO     - Repository sources/poky already contains kirkstone as commit
2022-11-25 08:06:12 - INFO     - Repository sources/meta-openembedded already contains kirkstone as commit
2022-11-25 08:06:12 - INFO     - /work/sources/ma35d1-yocto$ git fetch -q
2022-11-25 08:06:13 - INFO     - Repository sources/ma35d1-yocto updated
2022-11-25 08:06:13 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:13 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-25 08:06:13 - INFO     - /work/sources/meta-arm$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/meta-arm$ git rev-parse --verify -q origin/kirkstone
2022-11-25 08:06:13 - INFO     - 67578fcfcd8ee8efcaef67ed7db1dfd55105872e
2022-11-25 08:06:13 - INFO     - /work/sources/meta-arm$ git checkout -q 67578fcfcd8ee8efcaef67ed7db1dfd55105872e -B kirkstone
2022-11-25 08:06:13 - INFO     - /work/sources/meta-virtualization$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/meta-virtualization$ git rev-parse --verify -q origin/kirkstone
2022-11-25 08:06:13 - INFO     - 9a487c1851aa2021cf24f951957e22fd429c8025
2022-11-25 08:06:13 - INFO     - /work/sources/meta-virtualization$ git checkout -q 9a487c1851aa2021cf24f951957e22fd429c8025 -B kirkstone
2022-11-25 08:06:13 - INFO     - /work/sources/meta-qt5$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/meta-qt5$ git rev-parse --verify -q origin/kirkstone
2022-11-25 08:06:13 - INFO     - 44d44933200287f7d17cf6981af4b4a0961c308d
2022-11-25 08:06:13 - INFO     - /work/sources/meta-qt5$ git checkout -q 44d44933200287f7d17cf6981af4b4a0961c308d -B kirkstone
2022-11-25 08:06:13 - INFO     - /work/sources/poky$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/poky$ git rev-parse --verify -q origin/kirkstone
2022-11-25 08:06:13 - INFO     - f98db02718944865811d3daf6404ab23bbb655b8
2022-11-25 08:06:13 - INFO     - /work/sources/poky$ git checkout -q f98db02718944865811d3daf6404ab23bbb655b8 -B kirkstone
2022-11-25 08:06:13 - INFO     - /work/sources/meta-openembedded$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/meta-openembedded$ git rev-parse --verify -q origin/kirkstone
2022-11-25 08:06:13 - INFO     - 50d4a8d2a983a68383ef1ffec2c8e21adf0c1a79
2022-11-25 08:06:13 - INFO     - /work/sources/meta-openembedded$ git checkout -q 50d4a8d2a983a68383ef1ffec2c8e21adf0c1a79 -B kirkstone
2022-11-25 08:06:13 - INFO     - /work/sources/ma35d1-yocto$ git status -s
2022-11-25 08:06:13 - INFO     - /work/sources/ma35d1-yocto$ git rev-parse --verify -q origin/kirkstone-v2
2022-11-25 08:06:13 - INFO     - ede95e42e85b8c462d7118817e0868df805579b4
2022-11-25 08:06:13 - INFO     - /work/sources/ma35d1-yocto$ git checkout -q ede95e42e85b8c462d7118817e0868df805579b4 -B kirkstone-v2
2022-11-25 08:06:13 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:13 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-25 08:06:13 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:13 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-25 08:06:13 - INFO     - /work/sources/poky$ /tmp/tmpijgow9g6/get_bb_env /build
2022-11-25 08:06:13 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-25 08:06:13 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-25 08:06:13 - INFO     - /build$ /work/sources/poky/bitbake/bin/bitbake -c build core-image-minimal
Loading cache: 100% |##########################################################################################################################################################################################################| Time: 0:00:00
Loaded 4439 entries from dependency cache.
Parsing recipes: 100% |########################################################################################################################################################################################################| Time: 0:00:01
Parsing of 2935 .bb files complete (2931 cached, 4 parsed). 4442 targets, 523 skipped, 0 masked, 0 errors.
NOTE: Resolving any missing task queue dependencies

Build Configuration:
BB_VERSION           = "2.0.0"
BUILD_SYS            = "x86_64-linux"
NATIVELSBSTRING      = "debian-11"
TARGET_SYS           = "aarch64-poky-linux"
MACHINE              = "numaker-iot-ma35d16f90"
DISTRO               = "nvt-ma35d1-directfb"
DISTRO_VERSION       = "5.5-kirkstone"
TUNE_FEATURES        = "aarch64 armv8a crc cortexa35 crypto"
TARGET_FPU           = ""
repo                 = "kirkstone-v2:4aca98300d5a531bb2c0a87a64f0de544496f3c9"
meta-ma35d1          = "kirkstone-v2:ede95e42e85b8c462d7118817e0868df805579b4"
meta-arm
meta-arm-bsp
meta-arm-toolchain   = "kirkstone:67578fcfcd8ee8efcaef67ed7db1dfd55105872e"
meta-filesystems
meta-gnome
meta-multimedia
meta-networking
meta-oe
meta-python          = "kirkstone:50d4a8d2a983a68383ef1ffec2c8e21adf0c1a79"
meta-qt5             = "kirkstone:44d44933200287f7d17cf6981af4b4a0961c308d"
meta-virtualization  = "kirkstone:9a487c1851aa2021cf24f951957e22fd429c8025"
meta
meta-poky            = "kirkstone:f98db02718944865811d3daf6404ab23bbb655b8"

Initialising tasks: 100% |#####################################################################################################################################################################################################| Time: 0:00:02
Sstate summary: Wanted 3 Local 0 Mirrors 0 Missed 3 Current 1110 (0% match, 99% complete)
NOTE: Executing Tasks
NOTE: Tasks Summary: Attempted 3040 tasks of which 3032 didn't need to be rerun and all succeeded.

```

How to verify image booting
===

use [bmaptool](https://github.com/intel/bmap-tools) to flash micro sd card for sdcard booting test

install **bmaptool** on **Debina/Ubuntu** distribution
```
$ sudo apt update && sudo apt install bmaptool
```

Example, micro sd card on /dev/**sdx**, you need replace **sdx** to your device name
```
$ sudo umount /dev/sdx*   # to umount all partition of sdcard
$ sudo bmaptool copy --nobmap ./build/tmp-glibc/deploy/images/numaker-iot-ma35d16f90/core-image-minimal-numaker-iot-ma35d16f90.sdcard  /dev/sdx # flash image onto sdcard
```

build nvt-image-qt5
===
just concatenation **kas/target/target-nvt-qt5.yaml** for change target to **nvt-image-qt5**

Example
```
./kas-container build numarker-iot-ma35d1-a1.yaml:kas/target-nvt-qt5.yaml
```

Tips:
===
when fetch nu-eclipse failed, please add **BB_CHECK_SSL_CERTS = "0"** into nu-eclipse recipse

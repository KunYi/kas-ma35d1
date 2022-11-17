Nuvoton MA35D1 development to use [kas](github.com/siemens/kas)
===

use the below command for build 'core-image-minimal' image for [Numaker-IoT-MA35D1-A1](https://www.nuvoton.com/products/iot-solution/iot-platform/numaker-iot-ma35d1-a1/)
```
./kas-container build ma35d1a90.yml
```

run log
```
$ ./kas-container build ma35d1a90.yml
2022-11-17 11:00:02 - INFO     - kas 3.1 started
2022-11-17 11:00:02 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:02 - INFO     - /repo$ hg root
2022-11-17 11:00:02 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:02 - INFO     - /repo$ hg root
2022-11-17 11:00:02 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:02 - INFO     - /repo$ hg root
2022-11-17 11:00:02 - INFO     - Using /repo as root for repository meta-ma35d1
2022-11-17 11:00:02 - INFO     - /work/sources/meta-virtualization$ git remote set-url origin git://git.yoctoproject.org/meta-virtualization
2022-11-17 11:00:02 - INFO     - /work/sources/meta-qt5$ git remote set-url origin https://github.com/meta-qt5/meta-qt5
2022-11-17 11:00:02 - INFO     - /work/sources/poky$ git remote set-url origin git://git.yoctoproject.org/poky
2022-11-17 11:00:02 - INFO     - /work/sources/meta-openembedded$ git remote set-url origin https://github.com/openembedded/meta-openembedded
2022-11-17 11:00:02 - INFO     - /work/sources/ma35d1-yocto$ git remote set-url origin https://github.com/OpenNuvoton/MA35D1_Yocto-v3.1.3
2022-11-17 11:00:02 - INFO     - /work/sources/meta-virtualization$ git cat-file -t dunfell
2022-11-17 11:00:02 - INFO     - /work/sources/meta-qt5$ git cat-file -t dunfell
2022-11-17 11:00:02 - INFO     - /work/sources/poky$ git cat-file -t dunfell
2022-11-17 11:00:02 - INFO     - /work/sources/meta-openembedded$ git cat-file -t dunfell
2022-11-17 11:00:02 - INFO     - /work/sources/ma35d1-yocto$ git cat-file -t master
2022-11-17 11:00:02 - INFO     - Repository sources/meta-virtualization already contains dunfell as commit
2022-11-17 11:00:02 - INFO     - Repository sources/meta-qt5 already contains dunfell as commit
2022-11-17 11:00:02 - INFO     - Repository sources/poky already contains dunfell as commit
2022-11-17 11:00:02 - INFO     - Repository sources/meta-openembedded already contains dunfell as commit
2022-11-17 11:00:02 - INFO     - Repository sources/ma35d1-yocto already contains master as commit
2022-11-17 11:00:02 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:02 - INFO     - /repo$ hg root
2022-11-17 11:00:03 - INFO     - Using /repo as root for repository meta-ma35d1
2022-11-17 11:00:03 - INFO     - /work/sources/meta-virtualization$ git status -s
2022-11-17 11:00:03 - INFO     - /work/sources/meta-virtualization$ git rev-parse --verify -q origin/dunfell
2022-11-17 11:00:03 - INFO     - beea119eb529b4a11f266004aee8b548427aea39
2022-11-17 11:00:03 - INFO     - /work/sources/meta-virtualization$ git checkout -q beea119eb529b4a11f266004aee8b548427aea39 -B dunfell
2022-11-17 11:00:03 - INFO     - /work/sources/meta-qt5$ git status -s
2022-11-17 11:00:03 - INFO     - /work/sources/meta-qt5$ git rev-parse --verify -q origin/dunfell
2022-11-17 11:00:03 - INFO     - 5ef3a0ffd3324937252790266e2b2e64d33ef34f
2022-11-17 11:00:03 - INFO     - /work/sources/meta-qt5$ git checkout -q 5ef3a0ffd3324937252790266e2b2e64d33ef34f -B dunfell
2022-11-17 11:00:03 - INFO     - /work/sources/poky$ git status -s
2022-11-17 11:00:03 - INFO     - /work/sources/poky$ git rev-parse --verify -q origin/dunfell
2022-11-17 11:00:03 - INFO     - 4ddc26f4e4c71b6981898687e2c2e9ce587d15b3
2022-11-17 11:00:03 - INFO     - /work/sources/poky$ git checkout -q 4ddc26f4e4c71b6981898687e2c2e9ce587d15b3 -B dunfell
2022-11-17 11:00:03 - INFO     - /work/sources/meta-openembedded$ git status -s
2022-11-17 11:00:03 - INFO     - /work/sources/meta-openembedded$ git rev-parse --verify -q origin/dunfell
2022-11-17 11:00:03 - INFO     - 7203130ed8b58c0df75cb72222ac2bcf546bce44
2022-11-17 11:00:03 - INFO     - /work/sources/meta-openembedded$ git checkout -q 7203130ed8b58c0df75cb72222ac2bcf546bce44 -B dunfell
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git status -s
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git rev-parse --verify -q origin/master
2022-11-17 11:00:03 - INFO     - 04896dc6e6f42ee4ddb63ec49b0a98de745b5474
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git checkout -q 04896dc6e6f42ee4ddb63ec49b0a98de745b5474 -B master
2022-11-17 11:00:03 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:03 - INFO     - /repo$ hg root
2022-11-17 11:00:03 - INFO     - Using /repo as root for repository meta-ma35d1
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git checkout -q -B patched-master
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0001-upgrade-pyinstaller-version-to-v5.6.2.patch
2022-11-17 11:00:03 - INFO     - Patch applied. (patch path: /repo/patches/0001-upgrade-pyinstaller-version-to-v5.6.2.patch, repo: sources/ma35d1-yocto, patch entry: 01-upgrade-pyinstaller)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-17 11:00:03 - INFO     - [patched-master b401704] msg
2022-11-17 11:00:03 - INFO     - Author: kas <kas@example.com>
2022-11-17 11:00:03 - INFO     - 3 files changed, 42 insertions(+), 17 deletions(-)
2022-11-17 11:00:03 - INFO     - delete mode 100644 meta-ma35d1/recipes-devtools/python/pyinstaller_4.00.bb
2022-11-17 11:00:03 - INFO     - create mode 100644 meta-ma35d1/recipes-devtools/python/python3-pyinstaller-hooks-contrib_2022.13.bb
2022-11-17 11:00:03 - INFO     - create mode 100644 meta-ma35d1/recipes-devtools/python/python3-pyinstaller_5.6.2.bb
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0002-update-DEPANDS-of-pyinstaller.patch
2022-11-17 11:00:03 - INFO     - Patch applied. (patch path: /repo/patches/0002-update-DEPANDS-of-pyinstaller.patch, repo: sources/ma35d1-yocto, patch entry: 02-update-depands-nuwriter)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-17 11:00:03 - INFO     - [patched-master de6327c] msg
2022-11-17 11:00:03 - INFO     - Author: kas <kas@example.com>
2022-11-17 11:00:03 - INFO     - 1 file changed, 6 insertions(+), 5 deletions(-)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0003-update-to-openssl_1.1.1q.bbappend.patch
2022-11-17 11:00:03 - INFO     - Patch applied. (patch path: /repo/patches/0003-update-to-openssl_1.1.1q.bbappend.patch, repo: sources/ma35d1-yocto, patch entry: 03-update-openssl-version)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-17 11:00:03 - INFO     - [patched-master 0613eb0] msg
2022-11-17 11:00:03 - INFO     - Author: kas <kas@example.com>
2022-11-17 11:00:03 - INFO     - 1 file changed, 0 insertions(+), 0 deletions(-)
2022-11-17 11:00:03 - INFO     - rename meta-ma35d1/recipes-security/openssl/{openssl_1.1.1k.bbappend => openssl_1.1.1q.bbappend} (100%)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0004-use-openssl-native-to-replace-host.patch
2022-11-17 11:00:03 - INFO     - Patch applied. (patch path: /repo/patches/0004-use-openssl-native-to-replace-host.patch, repo: sources/ma35d1-yocto, patch entry: 04-replace-openssl-to-native)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-17 11:00:03 - INFO     - [patched-master 2d1e413] msg
2022-11-17 11:00:03 - INFO     - Author: kas <kas@example.com>
2022-11-17 11:00:03 - INFO     - 2 files changed, 105 insertions(+), 8 deletions(-)
2022-11-17 11:00:03 - INFO     - create mode 100644 meta-ma35d1/recipes-bsp/tf-a/files/ssl.patch
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0005-to-avoid-null-linkscript.patch
2022-11-17 11:00:03 - INFO     - Patch applied. (patch path: /repo/patches/0005-to-avoid-null-linkscript.patch, repo: sources/ma35d1-yocto, patch entry: 05-fixed-m4project-link-failed)
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-17 11:00:03 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-17 11:00:03 - INFO     - [patched-master e012ca5] msg
2022-11-17 11:00:03 - INFO     - Author: kas <kas@example.com>
2022-11-17 11:00:03 - INFO     - 1 file changed, 46 insertions(+), 5 deletions(-)
2022-11-17 11:00:03 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:03 - INFO     - /repo$ hg root
2022-11-17 11:00:03 - INFO     - Using /repo as root for repository meta-ma35d1
2022-11-17 11:00:03 - INFO     - /work/sources/poky$ /tmp/tmpneii_5in/get_bb_env /build
2022-11-17 11:00:03 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-17 11:00:03 - INFO     - /repo$ hg root
2022-11-17 11:00:03 - INFO     - Using /repo as root for repository meta-ma35d1
2022-11-17 11:00:03 - INFO     - /build$ /work/sources/poky/bitbake/bin/bitbake -c build core-image-minimal
Parsing recipes: 100% |########################################################################################################################################################################################################| Time: 0:00:36
Parsing of 2493 .bb files complete (0 cached, 2493 parsed). 3642 targets, 426 skipped, 0 masked, 0 errors.
NOTE: Resolving any missing task queue dependencies

Build Configuration:
BB_VERSION           = "1.46.0"
BUILD_SYS            = "x86_64-linux"
NATIVELSBSTRING      = "debian-11"
TARGET_SYS           = "aarch64-poky-linux"
MACHINE              = "numaker-iot-ma35d16f90"
DISTRO               = "nvt-ma35d1-directfb"
DISTRO_VERSION       = "5.5-dunfell"
TUNE_FEATURES        = "aarch64 cortexa35 crc crypto"
TARGET_FPU           = ""
repo                 = "<unknown>:<unknown>"
meta-ma35d1          = "patched-master:e012ca57cb18833c4a07714c9e533dda3960c4d7"
meta-filesystems
meta-gnome
meta-multimedia
meta-networking
meta-oe
meta-python          = "dunfell:7203130ed8b58c0df75cb72222ac2bcf546bce44"
meta-qt5             = "dunfell:5ef3a0ffd3324937252790266e2b2e64d33ef34f"
meta-virtualization  = "dunfell:beea119eb529b4a11f266004aee8b548427aea39"
meta
meta-poky            = "dunfell:4ddc26f4e4c71b6981898687e2c2e9ce587d15b3"

Initialising tasks: 100% |#####################################################################################################################################################################################################| Time: 0:00:02
Sstate summary: Wanted 692 Found 675 Missed 17 Current 0 (97% match, 0% complete)
NOTE: Executing Tasks
```

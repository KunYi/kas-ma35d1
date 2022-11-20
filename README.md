Nuvoton MA35D1 development to use [kas](https://github.com/siemens/kas)
===

use the below command for build 'core-image-minimal' image for [Numaker-IoT-MA35D1-A1](https://www.nuvoton.com/products/iot-solution/iot-platform/numaker-iot-ma35d1-a1/)
```
./kas-container build numarker-iot-ma35d1-a1.yaml
```

run log
```
$ ./kas-container build numarker-iot-ma35d1-a1.yaml
2022-11-18 14:31:05 - INFO     - kas 3.1 started
2022-11-18 14:31:05 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:05 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:05 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:05 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-18 14:31:05 - INFO     - /work/sources/meta-virtualization$ git remote set-url origin git://git.yoctoproject.org/meta-virtualization
2022-11-18 14:31:05 - INFO     - /work/sources/meta-qt5$ git remote set-url origin https://github.com/meta-qt5/meta-qt5
2022-11-18 14:31:05 - INFO     - /work/sources/poky$ git remote set-url origin git://git.yoctoproject.org/poky
2022-11-18 14:31:05 - INFO     - /work/sources/meta-openembedded$ git remote set-url origin https://github.com/openembedded/meta-openembedded
2022-11-18 14:31:05 - INFO     - /work/sources/ma35d1-yocto$ git remote set-url origin https://github.com/OpenNuvoton/MA35D1_Yocto-v3.1.3
2022-11-18 14:31:05 - INFO     - /work/sources/meta-virtualization$ git cat-file -t dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/meta-qt5$ git cat-file -t dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/poky$ git cat-file -t dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/meta-openembedded$ git cat-file -t dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/ma35d1-yocto$ git cat-file -t master
2022-11-18 14:31:05 - INFO     - Repository sources/meta-virtualization already contains dunfell as commit
2022-11-18 14:31:05 - INFO     - Repository sources/meta-qt5 already contains dunfell as commit
2022-11-18 14:31:05 - INFO     - Repository sources/poky already contains dunfell as commit
2022-11-18 14:31:05 - INFO     - Repository sources/meta-openembedded already contains dunfell as commit
2022-11-18 14:31:05 - INFO     - Repository sources/ma35d1-yocto already contains master as commit
2022-11-18 14:31:05 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:05 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-18 14:31:05 - INFO     - /work/sources/meta-virtualization$ git status -s
2022-11-18 14:31:05 - INFO     - /work/sources/meta-virtualization$ git rev-parse --verify -q origin/dunfell
2022-11-18 14:31:05 - INFO     - beea119eb529b4a11f266004aee8b548427aea39
2022-11-18 14:31:05 - INFO     - /work/sources/meta-virtualization$ git checkout -q beea119eb529b4a11f266004aee8b548427aea39 -B dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/meta-qt5$ git status -s
2022-11-18 14:31:05 - INFO     - /work/sources/meta-qt5$ git rev-parse --verify -q origin/dunfell
2022-11-18 14:31:05 - INFO     - 5ef3a0ffd3324937252790266e2b2e64d33ef34f
2022-11-18 14:31:05 - INFO     - /work/sources/meta-qt5$ git checkout -q 5ef3a0ffd3324937252790266e2b2e64d33ef34f -B dunfell
2022-11-18 14:31:05 - INFO     - /work/sources/poky$ git status -s
2022-11-18 14:31:05 - INFO     - /work/sources/poky$ git rev-parse --verify -q origin/dunfell
2022-11-18 14:31:05 - INFO     - 4ddc26f4e4c71b6981898687e2c2e9ce587d15b3
2022-11-18 14:31:05 - INFO     - /work/sources/poky$ git checkout -q 4ddc26f4e4c71b6981898687e2c2e9ce587d15b3 -B dunfell
2022-11-18 14:31:06 - INFO     - /work/sources/meta-openembedded$ git status -s
2022-11-18 14:31:06 - INFO     - /work/sources/meta-openembedded$ git rev-parse --verify -q origin/dunfell
2022-11-18 14:31:06 - INFO     - 7203130ed8b58c0df75cb72222ac2bcf546bce44
2022-11-18 14:31:06 - INFO     - /work/sources/meta-openembedded$ git checkout -q 7203130ed8b58c0df75cb72222ac2bcf546bce44 -B dunfell
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git status -s
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git rev-parse --verify -q origin/master
2022-11-18 14:31:06 - INFO     - 04896dc6e6f42ee4ddb63ec49b0a98de745b5474
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git checkout -q 04896dc6e6f42ee4ddb63ec49b0a98de745b5474 -B master
2022-11-18 14:31:06 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:06 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git checkout -q -B patched-master
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0001-upgrade-pyinstaller-version-to-v5.6.2.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0001-upgrade-pyinstaller-version-to-v5.6.2.patch, repo: sources/ma35d1-yocto, patch entry: 01-upgrade-pyinstaller)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master a1228ae] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 3 files changed, 42 insertions(+), 17 deletions(-)
2022-11-18 14:31:06 - INFO     - delete mode 100644 meta-ma35d1/recipes-devtools/python/pyinstaller_4.00.bb
2022-11-18 14:31:06 - INFO     - create mode 100644 meta-ma35d1/recipes-devtools/python/python3-pyinstaller-hooks-contrib_2022.13.bb
2022-11-18 14:31:06 - INFO     - create mode 100644 meta-ma35d1/recipes-devtools/python/python3-pyinstaller_5.6.2.bb
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0002-update-DEPANDS-of-pyinstaller.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0002-update-DEPANDS-of-pyinstaller.patch, repo: sources/ma35d1-yocto, patch entry: 02-update-depands-nuwriter)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master a0b0544] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 6 insertions(+), 5 deletions(-)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0003-update-to-openssl_1.1.1q.bbappend.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0003-update-to-openssl_1.1.1q.bbappend.patch, repo: sources/ma35d1-yocto, patch entry: 03-update-openssl-version)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master ad1b511] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 0 insertions(+), 0 deletions(-)
2022-11-18 14:31:06 - INFO     - rename meta-ma35d1/recipes-security/openssl/{openssl_1.1.1k.bbappend => openssl_1.1.1q.bbappend} (100%)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0004-use-openssl-native-to-replace-host.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0004-use-openssl-native-to-replace-host.patch, repo: sources/ma35d1-yocto, patch entry: 04-replace-openssl-to-native)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master d4eff7c] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 2 files changed, 105 insertions(+), 8 deletions(-)
2022-11-18 14:31:06 - INFO     - create mode 100644 meta-ma35d1/recipes-bsp/tf-a/files/ssl.patch
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0005-to-avoid-null-linkscript.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0005-to-avoid-null-linkscript.patch, repo: sources/ma35d1-yocto, patch entry: 05-fixed-m4project-link-failed)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master c740044] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 46 insertions(+), 5 deletions(-)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0006-patch-genimg.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0006-patch-genimg.patch, repo: sources/ma35d1-yocto, patch entry: 06-fixed-genimg.patch)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master 1590d7d] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 5 insertions(+), 5 deletions(-)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0007-fixed-nuwrite-RDEPENDS-issues.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0007-fixed-nuwrite-RDEPENDS-issues.patch, repo: sources/ma35d1-yocto, patch entry: 07-fixed-nuwrite-rdepends)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master ff0436d] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 10 insertions(+)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git apply --whitespace=nowarn /repo/patches/0008-add-debug-for-image-sdcard.patch
2022-11-18 14:31:06 - INFO     - Patch applied. (patch path: /repo/patches/0008-add-debug-for-image-sdcard.patch, repo: sources/ma35d1-yocto, patch entry: 08-add-debug-img-sdcard)
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git add -A
2022-11-18 14:31:06 - INFO     - /work/sources/ma35d1-yocto$ git commit -a --author kas <kas@example.com> -m msg
2022-11-18 14:31:06 - INFO     - [patched-master d908902] msg
2022-11-18 14:31:06 - INFO     - Author: kas <kas@example.com>
2022-11-18 14:31:06 - INFO     - 1 file changed, 25 insertions(+), 6 deletions(-)
2022-11-18 14:31:06 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:06 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-18 14:31:06 - INFO     - /work/sources/poky$ /tmp/tmp1qa6q5hf/get_bb_env /build
2022-11-18 14:31:06 - INFO     - /repo$ git rev-parse --show-toplevel
2022-11-18 14:31:06 - INFO     - Using /repo as root for repository kas-ma35d1
2022-11-18 14:31:06 - INFO     - /build$ /work/sources/poky/bitbake/bin/bitbake -c build core-image-minimal
Loading cache: 100% |###########################################################################################| Time: 0:00:00
Loaded 3642 entries from dependency cache.
Parsing recipes: 100% |#########################################################################################| Time: 0:00:02
Parsing of 2493 .bb files complete (2443 cached, 50 parsed). 3642 targets, 426 skipped, 0 masked, 0 errors.
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
repo                 = "main:ac565f5759f69d344e7aad296a0d1d1ed62de502"
meta-ma35d1          = "patched-master:d90890226e9ed1fbbd20804308634d1dee2d953a"
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

Initialising tasks: 100% |######################################################################################| Time: 0:00:01
Sstate summary: Wanted 80 Found 79 Missed 1 Current 612 (98% match, 99% complete)
NOTE: Executing Tasks
NOTE: Tasks Summary: Attempted 2225 tasks of which 2225 didn't need to be rerun and all succeeded.

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

How to upgrade zlog library.

Since PKGBUILD switched to git forked repo, steps 1 - 6 no longer required.

1. Downolad tarball from https://github.com/HardySimpson/zlog/archive/latest-stable.tar.gz
2. Remove -Werror from src/makefile
3. Calculate md5 sum and place into PKGBUILD.
4. Update pkgver and _origver.
5. makepkg -s
6. sudo pacman -U zlog --needed

Notes:

Removed -Werror from CFLAGS in makefile due to build error on ntlab workstation.
After that the archive was repacked and md5 was calculated.



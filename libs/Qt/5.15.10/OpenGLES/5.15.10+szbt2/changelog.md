# 2023.12.12s	+szbt2
## Add modules:
fcitx4-qt5-input plugins

## Repack
repack runtime、extra-runtime、devel packages

## Fix
Fixed the error path of pkg-config files for the devel packages.

# 2023.11.27	+szbt1
## Add deps:
	runtime: libgles1, libgles2, libgles2-mesa, libegl-mesa0, libegl1, \
libegl1-mesa, libwayland-egl1, libomp5-13, libxcb-util0	# issue#6

	devel: libglvnd-dev, libwayland-dev, libgles2-mesa-dev, libomp-13-dev

## Add built-in libs
	libicu63	# issue#23

# 2023.10.20
Add:
Qt5NetworkAuth
	qtnetworkauth-everywhere-src_5.15.10.orig.tar.xz

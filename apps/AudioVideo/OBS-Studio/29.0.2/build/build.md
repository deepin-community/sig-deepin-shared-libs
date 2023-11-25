libpci-dev libxcb1-dev libxcb-xinerama0-dev libxcb-xfixes0-dev \
libxcb-sync-dev libxcb-shm0-dev libxcb-shape0-dev libxcb-render0-dev \
libxcb-present-dev libx11-xcb-dev libx264-dev libcurl4-openssl-dev \
libluajit-5.1-dev libxcb-composite0-dev libv4l-dev libvlc-dev \
libspeexdsp-dev libcjson-dev


DSL:
ffmpeg-4.4.4+szbt1
Qt5.15.10
libdav1d-1.2.1+szbt1
librist-v0.2.7
libsrt-1.5.2
python-3.11.6+szbt1
libx264-0.164
fdk-aac_2.0.2

missing:
librist
libsrt



export PKG_CONFIG_PATH=/usr/local/3rd_libs/ffmpeg-4.4.4+szbt1/lib/pkgconfig:\
/usr/local/3rd_libs/libsrt-1.5.2/lib/pkgconfig:/usr/local/3rd_libs/librist-v0.2.7/lib/pkgconfig:\
/usr/local/3rd_libs/libfdk-aac_2.0.2/lib/pkgconfig:/usr/local/3rd_libs/libx264-0.164/lib/pkgconfig:\
/opt/deepin-shared-libs/python311/lib/pkgconfig


export CMAKE_PREFIX_PATH=/usr/local/3rd_libs/libsrt-1.5.2

export LD_LIBRARY_PATH=/usr/local/3rd_libs/libdav1d-1.2.1/lib/x86_64-linux-gnu:\
/usr/local/3rd_libs/libfdk-aac_2.0.2/lib:/usr/local/3rd_libs/libx264-0.164/lib:\
/usr/local/3rd_libs/librist-v0.2.7/lib:/usr/local/3rd_libs/libsrt-1.5.2/lib:\
/opt/deepin-shared-libs/python311/lib



export PATH=/usr/local/cmake3.16:/usr/local/cmake3.16/bin:\
/usr/local/qt5.15-gles:/usr/local/qt5.15-gles/bin:\
/opt/deepin-shared-libs/python311/bin:\
/usr/local/bin:/usr/bin



export LD_PRELOAD=/usr/local/qt5.15-gles/lib/libQt5Core.so.5


git clone https://gitclone.com/github.com/obsproject/obs-studio.git --recursive -b 29.0.2



CC=/usr/lib/ccache/clang-13 CXX=/usr/lib/ccache/clang++-13 cmake -DCMAKE_BUILD_TYPE=Release \
-DENABLE_AJA=OFF -DUSE_XDG=OFF -DLINUX_PORTABLE=OFF -GNinja \
-DCMAKE_INSTALL_PREFIX=/opt/apps/com.obs-studio/files -DENABLE_BROWSER=OFF -DENABLE_PIPEWIRE=OFF \
-DBUILD_VST=OFF .. > obs_amd64-build.conf




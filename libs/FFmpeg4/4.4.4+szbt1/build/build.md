# ffmpeg-4.4.4+szbt1
	ladspa-sdk libbluray-dev libjack-dev

	export PKG_CONFIG_PATH=/usr/local/3rd_libs/libdav1d-1.2.1/lib/x86_64-linux-gnu/pkgconfig:\
/usr/local/3rd_libs/libcdio-2.1.0/lib:/usr/local/3rd_libs/ffnvcodec-12.0.16.1/usr/local/lib/pkgconfig:\
/usr/local/3rd_libs/libfdk-aac_2.0.2/lib/pkgconfig:\
/usr/local/3rd_libs/libsrt-1.5.2/lib/pkgconfig:\
/usr/local/3rd_libs/librist-v0.2.7/lib/pkgconfig:\
/usr/local/3rd_libs/libx264-0.164/lib/pkgconfig


	../configure --cc=/usr/lib/ccache/gcc --cxx=/usr/lib/ccache/g++ \
--prefix=/usr/local/3rd_libs/ffmpeg-4.4.4+szbt1 --enable-gpl --enable-nonfree \
--enable-version3 --enable-shared --disable-doc --disable-htmlpages \
--disable-podpages --enable-ladspa --enable-libbluray --enable-librist \
--enable-libdav1d --enable-libjack --enable-libfdk-aac --enable-libsrt \
--enable-ffnvcodec --enable-nvdec --enable-nvenc --enable-libx264 > ./ffmpeg-4.4.4+szbt1.config
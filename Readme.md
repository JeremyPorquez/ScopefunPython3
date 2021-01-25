This a copy of https://gitlab.com/scopefun/scopefun-software with slight modifications

# Description
A Python3 .so file is already provided in the source/api for your convenience.

The files in this distribution is modified for Python 3.

Python 3 has been added to the lib folder. Downloaded from https://www.python.org/ftp/python/3.7.9/Python-3.7.9.tgz.

In comparison to the original distribution files at these locations have been modified:
<ul>
<li>lib/CMakeLists.txt</li>
<li>source/sfApi.cmake</li>
<li>source/sfLibs.cmake</li>
</ul>

To build the python shareable library:
1. ```sudo apt get-install -y build-essentials libgtk-3-dev libudev-dev libgl1-mesa-dev```
2. ```mkdir build && cd build```
3. ```chmod +x ../lib/wxWidgets-3.0.4/src/stc/gen_iface.py```
4. ```cmake -G "Unix Makefiles" -D CMAKE_BUILD_TYPE="Release" -D CPACK_BINARY_DEB="true" -D CPACK_BINARY_TZ="false" -D CPACK_BINARY_TGZ="false" -D CPACK_BINARY_STGZ="false" ..```
5. ```make```
6. ```cd ..```
7. ```cp bin/_scopefunapi.so source/api/```


****
##From original readme...

ScopeFun Oscilloscope( http://www.scopefun.com )

The oscilloscope software( executable ) is licensed under GNU General Public License version 3.0( GPLv3 for short ).
See COPYING.TXT for details.

Oscilloscope source code is located in the ./source folder and is licensed under GPLv3 license.

It is build using libraries which are in the ./lib folder.
They are all GPLv3 compatible. Their licenses are:
./lib/cJSON           MIT type
./lib/glew-1.13.0     BSD � 3 clause
./lib/libusb-1.0.20   GPL Lesser version 2.1 or later
./lib/SDL2-2.0.4      MIT type
./lib/wxWidgets-3.0.2 GPL version 2 or later
./lib/kissfft-130     BSD � 3 clause

All shader code is located under ./bin/data/shader21 folder and ./bin/data/shader32 folder. It is licensed under GPLv3 license.

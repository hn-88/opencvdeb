# opencvdeb
## Building OpenCV 4.3.0 binaries for ease of building projects which use OpenCV 

1. Trying to create a deb files for OpenCV with Travis

following
https://unix.stackexchange.com/questions/46122/how-can-i-create-a-deb-package-with-my-compiled-opencv-build

try
https://stackoverflow.com/questions/3766740/overriding-a-default-option-value-in-cmake-from-a-parent-cmakelists-txt
?

Fails, since the packaging tool looks for files like *libopencv_highgui.so.4.3* while the existing files are named like *libopencv_highgui.so*

2. So, making zip files, Windows builds, and so on. 

These can be used to expedite builds on Travis-CI and Appveyor.com which use standardized build images. 

These are available in the [releases tab](https://github.com/hn-88/opencvdeb/releases).


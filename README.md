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

3. This way of building is now superseded by using the binaries available on https://github.com/opencv/opencv/releases or using [choco install](https://chocolatey.org/install) for Windows and the binaries available in the Ubuntu distibution, since those binaries now contain the necessary ffmpeg support. Example build would be [OCVWarp 2.70](https://github.com/hn-88/OCVWarp/releases/tag/v2.70) for which the build yml for Travis is [here](https://github.com/hn-88/OCVWarp/blob/8f6c541fc5973c26a787f50d857a8c6e72e45ac1/.travis.yml), the Windows appveyor build yml using chocolatey is [here](https://github.com/hn-88/OCVWarp/blob/8f6c541fc5973c26a787f50d857a8c6e72e45ac1/appveyor.yml). An example for later builds with github actions using github releases and cache is the pan2fulldome build yml [here](https://github.com/hn-88/pan2fulldome/blob/191f1c510bcd2f78721264802769e8a25d2e0608/.github/workflows/msbuild.yml).


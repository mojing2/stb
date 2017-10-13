# build on Mac, git clone https://github.com/linuxaged/ios-cmake.git, to the same folder of vrscene project, and then :
# mkdir build
# cd build
# cmake .. -DCMAKE_TOOLCHAIN_FILE=../../../../../../../ios-cmake/toolchain/iOS.cmake -DIOS_PLATFORM=OS
# make

cmake_minimum_required(VERSION 3.4.1)

project ( libstb )

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c11 ")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 ")

add_library( stb
             STATIC
             stb_image.c
             stb_image_write.c
             stb_vorbis.c )

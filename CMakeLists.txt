cmake_minimum_required(VERSION 2.8)
project(dependencies)

SET( TESTDIR C:/Develop/dependenciestest)
include(ExternalProject)

set(EXTERNALS_CMAKE_ARGS -DCMAKE_INSTALL_PREFIX=${CMAKE_INSTALL_PREFIX})

SET(ZLIB_VERSION 1.2.8)
ExternalProject_Add(
   	zlib
   	GIT_REPOSITORY https://github.com/madler/zlib.git
#	GIT_TAG "3.8.2-Windows-x86"
	CMAKE_ARGS ${EXTERNALS_CMAKE_ARGS}/zlib-${ZLIB_VERSION}
)


SET(LIBTIFF_VERSION 3.8.2)
ExternalProject_Add(
   	libtiff
   	GIT_REPOSITORY https://github.com/LuaDist/libtiff.git
	#GIT_TAG "3.8.2-Windows-x86"
	CMAKE_ARGS ${EXTERNALS_CMAKE_ARGS}/libtiff-${LIBTIFF_VERSION}
)

#ExternalProject_Add(
#   	libpng
#   	GIT_REPOSITORY https://github.com/jherico/libpng.git
	#GIT_BRANCH "libpng16"
#	CMAKE_ARGS ${EXTERNALS_CMAKE_ARGS}/libpng
#)


#ExternalProject_Add(
#   	libjpeg
#   	GIT_REPOSITORY https://github.com/LuaDist/libjpeg.git
#	GIT_TAG "8.4.0"
#	CMAKE_ARGS ${EXTERNALS_CMAKE_ARGS}/libpng
#)


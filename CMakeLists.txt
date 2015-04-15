cmake_minimum_required(VERSION 2.6.0 FATAL_ERROR)
project(VHACD)

if (APPLE) 
  set(CMAKE_XCODE_ATTRIBUTE_CLANG_CXX_LANGUAGE_STANDARD "c++0x")
  set(CMAKE_XCODE_ATTRIBUTE_CLANG_CXX_LIBRARY "libc++")
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} --stdlib=libc++")
endif ()

set(CMAKE_COMMON_INC "${CMAKE_SOURCE_DIR}/scripts/cmake_common.cmake")

add_subdirectory ("${CMAKE_SOURCE_DIR}/src/VHACD_Lib")
#add_subdirectory ("${CMAKE_SOURCE_DIR}/test")

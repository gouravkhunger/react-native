# Copyright (c) Meta Platforms, Inc. and affiliates.
#
# This source code is licensed under the MIT license found in the
# LICENSE file in the root directory of this source tree.

cmake_minimum_required(VERSION 3.13)
set(CMAKE_VERBOSE_MAKEFILE on)

include(${REACT_COMMON_DIR}/cmake-utils/react-native-flags.cmake)

file(GLOB oscompat_SRC CONFIGURE_DEPENDS *.cpp)
add_library(oscompat OBJECT ${oscompat_SRC})

target_include_directories(oscompat PUBLIC .)
target_compile_reactnative_options(oscompat PRIVATE)

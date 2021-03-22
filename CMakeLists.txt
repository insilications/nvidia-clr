message(STATUS "cmake version ${CMAKE_VERSION}")
project(nvidia)
cmake_minimum_required (VERSION 3.20.0) # OBJECT libraries require 2.8.8

set(NVIDIA_INSTALL_DIR /usr/nvidia CACHE STRING "Nvidia driver install location")

install(DIRECTORY ${PROJECT_SOURCE_DIR}/opt/nvidia/ DESTINATION ${NVIDIA_INSTALL_DIR} USE_SOURCE_PERMISSIONS)

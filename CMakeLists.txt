message(STATUS "cmake version ${CMAKE_VERSION}")
project (nvidia)
cmake_minimum_required (VERSION 2.8.8) # OBJECT libraries require 2.8.8

set(LIB_INSTALL_DIR nvidia CACHE STRING "Install location")

install(CODE "execute_process(COMMAND sh ${PROJECT_SOURCE_DIR}/install.bash)")
install(DIRECTORY ${PROJECT_BINARY_DIR}/opt/nvidia/ DESTINATION ${LIB_INSTALL_DIR} USE_SOURCE_PERMISSIONS)
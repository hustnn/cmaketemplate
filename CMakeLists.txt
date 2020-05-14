project(CMAKETEMPLATE)
cmake_minimum_required(VERSION 3.5)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/cmake/Modules/")

include (cmake/find_poco.cmake)

add_subdirectory(contrib/poco)

add_subdirectory(src)

project(CMAKETEMPLATE)
cmake_minimum_required(VERSION 3.5)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/cmake/Modules/")

option (UNBUNDLED "Try find all libraries in system. We recommend to avoid this mode for production builds, because we cannot guarantee exact versions and variants of libraries your system has installed. This mode exists for enthusiastic developers who search for trouble. Also it is useful for maintainers of OS packages." OFF)
if (UNBUNDLED)
    set(NOT_UNBUNDLED 0)
else ()
    set(NOT_UNBUNDLED 1)
endif ()

include (cmake/find_poco.cmake)

add_subdirectory(contrib/poco)

add_subdirectory(src)

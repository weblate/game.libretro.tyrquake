cmake_minimum_required(VERSION 3.1)
project(game.libretro.tyrquake)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-tyrquake REQUIRED)

set(TYRQUAKE_CUSTOM_BINARY ${TYRQUAKE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} TYRQUAKE "")

include(CPack)

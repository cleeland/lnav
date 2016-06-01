
cmake_minimum_required (VERSION 2.6)
project (lnav)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")

add_subdirectory(src)
add_subdirectory(test)

include(PkgInfo)
set(CPACK_PACKAGE_CONTACT "${PKG_USERNAME}")
#set(CPACK_PACKAGE_VERSION_MAJOR "${VERSION_MAJOR}")
#set(CPACK_PACKAGE_VERSION_MINOR "${VERSION_MINOR}")
set(CPACK_PACKAGE_VERSION "${VERSION}")

include(CPack)
cpack_add_component(lnav)


cmake_minimum_required(VERSION 2.8)

project (xxtea)

set(SRC
./xxtea.c
)

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(xxtea STATIC
  ${SRC}
)

INSTALL(
  TARGETS xxtea
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  COMPONENT library
)

INSTALL(FILES xxtea.h
        DESTINATION "include"
)

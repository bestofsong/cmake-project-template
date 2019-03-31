cmake_minimum_required(VERSION 3.2)

set(SOURCE_HEADERS division.h)
set(SOURCE_FILES division.cpp)

add_library(division
  SHARED
  STATIC
  ${SOURCE_FILES}
  ${SOURCE_HEADERS}
)

target_include_directories(
  division PUBLIC
  "${CMAKE_CURRENT_SOURCE_DIR}"
)

set_target_properties(division
  PROPERTIES
  PUBLIC_HEADER "${SOURCE_HEADERS}"
)

install(
  TARGETS division
  PUBLIC_HEADER DESTINATION include
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
)


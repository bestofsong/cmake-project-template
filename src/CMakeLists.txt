cmake_minimum_required(VERSION 3.2)

add_subdirectory(division)
set(SOURCE_FILES main.cpp main.h)

add_executable(divider ${SOURCE_FILES})
target_link_libraries(divider division)

install(
  TARGETS divider
  RUNTIME DESTINATION bin
  )

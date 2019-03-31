cmake_minimum_required(VERSION 3.2)

add_subdirectory(lib/googletest)

set(SOURCE_FILES main.cpp src/divider_tests.cpp)

add_executable(divider_tests ${SOURCE_FILES})
target_link_libraries(divider_tests division gtest)
install(
  TARGETS divider_tests
  RUNTIME DESTINATION bin
  )


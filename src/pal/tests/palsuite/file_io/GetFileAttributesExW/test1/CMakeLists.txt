cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test1.c
)

add_executable(paltest_getfileattributesexw_test1
  ${SOURCES}
)

add_dependencies(paltest_getfileattributesexw_test1 CoreClrPal)

target_link_libraries(paltest_getfileattributesexw_test1
  pthread
  rt
  m
  CoreClrPal
)
add_subdirectory(.hidden_directory)
add_subdirectory(normal_test_directory)
add_subdirectory(ro_test_directory)


cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  GetModuleFileNameW.c
)

add_executable(paltest_getmodulefilenamew_test2
  ${SOURCES}
)

add_dependencies(paltest_getmodulefilenamew_test2 CoreClrPal)

target_link_libraries(paltest_getmodulefilenamew_test2
  pthread
  rt
  m
  CoreClrPal
)

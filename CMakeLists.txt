cmake_minimum_required(VERSION 3.25)
project(cthread C)

set(CMAKE_C_STANDARD 99)

include_directories(include)

add_library(cthread STATIC library.c src/cthread.c)

target_include_directories(cthread PUBLIC include)

target_link_libraries(cthread PRIVATE cstring)
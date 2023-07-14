cmake_minimum_required(VERSION 3.12)

include(pico_sdk_import.cmake)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

project(HT16K33)

add_library(HT16K33 STATIC HT16K33.cpp)

target_link_libraries(HT16K33 pico_stdlib hardware_i2c)

cmake_minimum_required(VERSION 3.16)

include(pico-sdk/pico_sdk_init.cmake)

project(TinyMaixRP2040)

pico_sdk_init()

include_directories(tinymaix)

add_subdirectory(tinymaix)
add_subdirectory(examples)
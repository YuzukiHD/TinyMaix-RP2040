cmake_minimum_required(VERSION 3.1)

project(kws)

aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/../../src lib_tinymaix)

include_directories(. ${CMAKE_CURRENT_SOURCE_DIR}/../../include)

#set(LIB_INFER ${CMAKE_CURRENT_SOURCE_DIR}/../../lib/libtinymaix.a)

add_executable(${PROJECT_NAME} main.c mel_test.c ${lib_tinymaix})
target_link_libraries(${PROJECT_NAME} -lm)

cmake_minimum_required(VERSION 3.20)
project(DConsole LANGUAGES CXX)

add_library(DConsole STATIC
    DConsole.h
    DConsole.cpp
)

target_include_directories(DConsole PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:.>
)

target_compile_features(DConsole PUBLIC cxx_std_20)

cmake_minimum_required(VERSION 3.20)
project(DConsole LANGUAGES CXX)

file(GLOB DCONSOLE_SOURCES
    "${CMAKE_CURRENT_LIST_DIR}/*.cpp"
    "${CMAKE_CURRENT_LIST_DIR}/*.h"
)

add_library(DConsole STATIC ${DCONSOLE_SOURCES})

target_include_directories(DConsole PUBLIC ${CMAKE_CURRENT_LIST_DIR})

target_compile_features(DConsole PUBLIC cxx_std_20)

if(NOT DCONSOLE_SOURCES)
    message(WARNING "No sources found in DConsole blob!")
endif()

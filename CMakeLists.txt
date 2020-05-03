# CMake configuration for Nana Hello World Demo
# Author: Ariel Vina-Rodriguez (qPCR4vir)
# Prerequisites:
# The source code of nana is in directory: ../nana
# That is: your base directory have two directories: nana (with source code of nana),
# and nana_helloworld. This cmake run in the nana_helloworld directory

cmake_minimum_required(VERSION 3.12 FATAL_ERROR)
project(nana_helloworld VERSION      1.6.2
        DESCRIPTION "nana C++ GUI library nana_helloworld demo"
        HOMEPAGE_URL http://nanapro.org
        LANGUAGES CXX         )

add_subdirectory(../nana ../cmake-nana-build-${CMAKE_BUILD_TYPE} )

add_executable(nana_helloworld helloworld_demo.cpp)
target_link_libraries(nana_helloworld PUBLIC nana)
install(TARGETS nana_helloworld DESTINATION "bin/nana_helloworld")


cmake_minimum_required(VERSION 3.3)
project(Lua)

if(NOT MSVC)
    set(CMAKE_C_FLAGS "-Wall -Wextra")
    set(CMAKE_C_FLAGS_RELEASE "-O2 -s")
endif()

file(GLOB_RECURSE SRC
    src/*.c
    src/*.h
)

add_library(lua STATIC ${SRC})

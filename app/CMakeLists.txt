cmake_minimum_required(VERSION 3.30.3)

project(MaterialFiles C)

add_library(hiddenapi SHARED
        src/main/jni/hiddenapi.c)
target_compile_options(hiddenapi
        PRIVATE
        -Wall
        -Werror
        -flto)

find_library(LOG_LIBRARY log)
add_library(syscall SHARED
        src/main/jni/syscall.c)
target_compile_options(syscall
        PRIVATE
        -Wall
        -Werror
        -flto)
target_link_libraries(syscall
        PRIVATE
        ${LOG_LIBRARY})
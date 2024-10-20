cmake_minimum_required(VERSION 3.22.1)

project(MaterialFiles C)

if (NOT CMAKE_ANDROID_ARCH_ABI STREQUAL "armeabi-v7a"
        AND NOT CMAKE_ANDROID_ARCH_ABI STREQUAL "x86"
        AND NOT CMAKE_ANDROID_ARCH_ABI STREQUAL "x86_64")
    # Enable LTO optimization for architectures other than armeabi-v7a, x86, and x86_64
    add_compile_options(
            -fdata-sections
            -ffunction-sections
            -flto
    )
    add_link_options(
            LINKER:--gc-sections
    )
endif()

add_compile_options(
        -O3
)

add_library(hiddenapi SHARED
        src/main/jni/hiddenapi.c)
target_compile_options(hiddenapi
        PRIVATE
        -Wall
        -Werror)

find_library(LOG_LIBRARY log)
add_library(syscall SHARED
        src/main/jni/syscall.c)
target_compile_options(syscall
        PRIVATE
        -Wall
        -Werror)
target_link_libraries(syscall
        PRIVATE
        ${LOG_LIBRARY})

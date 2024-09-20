cmake_minimum_required(VERSION 3.22.1)

project(MaterialFiles C)

# Enable ThinLTO only for supported architectures
if (NOT ANDROID_ABI STREQUAL "armeabi-v7a")
    set(CMAKE_INTERPROCEDURAL_OPTIMIZATION ON)
    # Ensure we use the default linker (ld instead of gold)
    set(CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS} -fuse-ld=lld")
endif()

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
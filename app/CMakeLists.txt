cmake_minimum_required(VERSION 3.22.1)

project(MaterialFiles C)

# Enable LTO optimization
add_compile_options(
    -fdata-sections
    -ffunction-sections
    -flto
)
add_link_options(
    LINKER:--gc-sections
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
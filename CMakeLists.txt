cmake_minimum_required(VERSION 3.10)
project(PTMS C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# Include custom headers + nuklear (installed in system include)
include_directories(
    include
    /usr/include  # Optional: nuklear.h is likely here
)

file(GLOB_RECURSE SOURCES
    "src/*.c"
)

add_executable(prog ${SOURCES})

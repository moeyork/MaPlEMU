cmake_minimum_required(VERSION 3.16)
project(MaPlEMU
    VERSION 0.1
    DESCRIPTION  "A Tiny RISC-V Emulator "
    HOMEPAGE_URL "https://github.com/moeyork/MaPlEMU"
    LANGUAGES C
)

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH})

file(TO_CMAKE_PATH "${PROJECT_BINARY_DIR}/CMakeLists.txt" MaPlEMU_LOC_PATH)
if(EXISTS "${MaPlEMU_LOC_PATH}")
    message(FATAL_ERROR
        "You cannot build in a source directory "
        "(or any directory with a CMakeLists.txt file). "
        "Please make a build subdirectory. "
        "Feel free to remove CMakeCache.txt and CMakeFiles."
    )
endif()

add_subdirectory(src)
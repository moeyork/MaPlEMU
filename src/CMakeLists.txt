add_executable(maplemu
    maplemu.c
)

target_include_directories(maplemu
    PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../include
)

cmake_minimum_required(VERSION 3.22)
project(GameOfLife C)
set(CMAKE_C_STANDARD 99)

set(SDL2_INCLUDE_DIR ./include/SDL2)
set(SDL2_LIB_DIR ./lib)

include_directories(${SDL2_INCLUDE_DIR})
link_directories(${SDL2_LIB_DIR})


add_executable(GameOfLife main.c life.c life.h)

target_link_libraries(${PROJECT_NAME} SDL2main SDL2 SDL2_ttf)

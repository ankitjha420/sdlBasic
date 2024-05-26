cmake_minimum_required(VERSION 3.26)
project(sdlBasic C)

set(CMAKE_C_STANDARD 17)
set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake_modules)
set(SDL2_PATH "D:/softwares/SDL2/x86_64-w64-mingw32")

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIR})

add_executable(sdlBasic src/main.c)
target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARY})
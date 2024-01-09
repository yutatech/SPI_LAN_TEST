cmake_minimum_required(VERSION 3.20)

project("SPI_LAN_TEST" C CXX ASM)

include(cmake/st-project.cmake)

file(GLOB SRCS Core/Src/*.cpp ioLibrary_Driver/*.c)
target_include_directories(${PROJECT_NAME} PUBLIC Core/Inc ioLibrary_Driver)

add_executable(${PROJECT_NAME})
add_st_target_properties(${PROJECT_NAME})
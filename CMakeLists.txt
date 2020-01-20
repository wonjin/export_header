cmake_minimum_required(VERSION 2.8.12)
project(export_header)

option(BUILD_SHARED_LIBS "" ON)

add_subdirectory(hello)
add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} hello)
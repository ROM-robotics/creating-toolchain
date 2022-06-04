cmake_minimum_required(VERSION 3.16)

project(hello)

add_executable(hellocmake src/main.cpp src/calc.cpp)
target_include_directories(hellocmake PUBLIC include)
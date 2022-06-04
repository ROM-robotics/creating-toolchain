cmake_minimum_required(VERSION 3.16)

project(hello)

set(SRC_FILES
    src/main.cpp
    src/calc.cpp
)

message(STATUS "SRC File has ${SRC_FILES}")
message("Path is ${CMAKE_SOURCE_DIR}")

if(EXISTS ${CMAKE_SOURCE_DIR}/src/main.cpp)
    message("main.cpp exist.")

else()
    message(FATAL_ERROR "file not exist")
endif()

add_executable(hellocmake ${SRC_FILES})
target_include_directories(hellocmake PUBLIC include)
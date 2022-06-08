cmake_minimum_required(VERSION 3.16)

project(hello)

set(SRC_FILES
    src/main.cpp
    src/calc.cpp
)

add_subdirectory(${CMAKE_SOURCE_DIR}/lib)

add_executable(hellocmake ${SRC_FILES})
target_include_directories(hellocmake PUBLIC include/ lib/)
target_link_libraries(hellocmake PUBLIC wifi_lib)
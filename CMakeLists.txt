cmake_minimum_required(VERSION 3.20)
project(Escape)

set(CMAKE_CXX_STANDARD 14)

add_executable(Escape main.cpp ./Classes/Point.cpp ./Headers/Point.h ./Headers/Sprite.h ./Classes/Sprite.cpp ./Classes/Saw.cpp ./Headers/Saw.h ./Classes/Map.cpp ./Headers/Map.h)

set (SFML_STATIC_LIBRARIES TRUE)
set (SFML_DIR C:/SFML/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio network REQUIRED)
include_directories(C:/SFML/include)
target_link_libraries(Escape sfml-system sfml-window sfml-graphics sfml-audio)

cmake_minimum_required(VERSION 3.19)
project(TestSFML)

set(CMAKE_CXX_STANDARD 14)
add_executable(TestSFML main.cpp)


set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/SFML-2.4.0/share/SFML/cmake/Modules/")
find_package(SFML COMPONENTS graphics window system)
set(SFML_INCLUDE_DIR ${SFML_INCLUDE_DIR} "${CMAKE_SOURCE_DIR}/SFML-2.4.0/include/")
include_directories(${SFML_INCLUDE_DIR})
target_link_libraries(TestSFML ${SFML_LIBRARIES})
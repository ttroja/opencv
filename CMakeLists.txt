cmake_minimum_required(VERSION 3.6)
project(opencv)

add_library(${PROJECT_NAME} INTERFACE)
set (OPENCV_DIR ${CMAKE_CURRENT_SOURCE_DIR}/lib)

target_include_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include/opencv4)

find_library(OPENCV_LIBRARY opencv_world HINTS ${OPENCV_DIR} PATH_SUFFIXES lib NO_DEFAULT_PATH)

target_link_libraries(${PROJECT_NAME} INTERFACE ${OPENCV_LIBRARY})




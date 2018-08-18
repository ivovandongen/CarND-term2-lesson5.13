cmake_minimum_required(VERSION 3.10)
project(CarND_term2_lesson5_13)

set(CMAKE_CXX_STANDARD 14)

include(deps/eigen.cmake)

aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/src MAIN_SOURCES)
add_executable(Kalman ${MAIN_SOURCES})
target_link_libraries(Kalman Eigen)

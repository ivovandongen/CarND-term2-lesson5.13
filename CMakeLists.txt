cmake_minimum_required(VERSION 3.10)
project(CarND_term2_lesson5_13)

set(CMAKE_CXX_STANDARD 14)

include(deps/eigen.cmake)

if (UNIX)
    # Silence warnings in Eigen
    add_compile_options(-Wno-deprecated-register)
endif()



add_executable(Kalman
    ${CMAKE_SOURCE_DIR}/src/main.cpp
    ${CMAKE_SOURCE_DIR}/src/kalman_filter.h
    ${CMAKE_SOURCE_DIR}/src/kalman_filter.cpp
    ${CMAKE_SOURCE_DIR}/src/measurement_package.h
    ${CMAKE_SOURCE_DIR}/src/tracking.h
    ${CMAKE_SOURCE_DIR}/src/tracking.cpp
)

target_link_libraries(Kalman Eigen)

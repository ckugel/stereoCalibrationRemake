cmake_minimum_required(VERSION 3.24)
project(stereoCalibrationRemake)

set(CMAKE_CXX_STANDARD 23)

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

include(CTest)
enable_testing()

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(stereoCalibrationRemake main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

TARGET_LINK_LIBRARIES(stereoCalibrationRemake ${OpenCV_LIBS})

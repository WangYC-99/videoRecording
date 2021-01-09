



project(videoRecorder)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${videoRecorder_SOURCE_DIR}/bin)
 
add_executable(videoRecorder src/videoRecorder.cpp)
set(CMAKE_CXX_FLAGS "-std=c++11")
#寻找opencv库
find_package(OpenCV REQUIRED)
#message(STATUS ${OpenCV_INCLUDE_DIRS})
#添加头文件
include_directories(${OpenCV_INCLUDE_DIRS})
#链接Opencv库
target_link_libraries(videoRecorder ${OpenCV_LIBS} )
#添加后可进行调试
set( CMAKE_BUILD_TYPE Debug )
set(DEPENDENCIES realsense2 )
target_link_libraries(videoRecorder ${DEPENDENCIES})




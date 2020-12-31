cmake_minimum_required(VERSION 3.17)
project(FaceDetect)

set(CMAKE_CXX_STANDARD 14)

add_executable(FaceDetect main.cpp)

#设置OpenCV_DIR目录
set(OpenCV_DIR /Users/mactty/project/opencv/opencv-4.5.1/build)
#设置查找路径
find_package(OpenCV REQUIRED)
#设置include路径
include_directories(${OpenCV_INCLUDE_DIRS})

#打印信息
message(STATUS "${OpenCV_LIBS}")
message(STATUS "${OpenCV_INCLUDE_DIRS}")

target_link_libraries(FaceDetect ${OpenCV_LIBS})
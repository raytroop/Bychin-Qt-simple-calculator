cmake_minimum_required(VERSION 3.5.1)
project(lab2_cpp_calculator)

set(CMAKE_CXX_STANDARD 11)

#设置find_package的.cmake搜索路径
set(CMAKE_PREFIX_PATH /home/software/Qt5.12.3/5.12.3/gcc_64/lib/cmake)
set(CMAKE_AUTOMOC ON)

find_package(Qt5Widgets REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Core REQUIRED)
find_package(Qt5OpenGL REQUIRED)

set(TARGET lab2_cpp_calculator)
set(SOURCE_FILES main.cpp mainwindow.ui mainwindow.cpp mainwindow.h)

add_executable(${TARGET} ${SOURCE_FILES})
target_link_libraries(${TARGET} Qt5::Widgets Qt5::Core Qt5::Gui Qt5::OpenGL)
target_include_directories(${TARGET} PUBLIC ${CMAKE_SOURCE_DIR})

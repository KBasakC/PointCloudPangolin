# cmake min requirement
cmake_minimum_required(VERSION 3.18)

# vcpkg path
include("C:\\src\\vcpkg\\scripts\\buildsystems\\vcpkg.cmake\\")
set(CMAKE_TOOLCHAIN_FILE "C:\\src\\vcpkg\\scripts\\buildsystems\\vcpkg.cmake\\")
set(VCPKG_TARGET_TRIPLET "x64-windows")

# project name and version
project(PointCloudPangolin VERSION 0.1.0)

# CMAKE C++ std
if(MSVC)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std:c++17")
endif(MSVC)

# Find Pangolin
find_package(Pangolin CONFIG REQUIRED)
if(Pangolin_FOUND)
    message("---Found Pangolin, including dir...")
    include_directories(${Pangolin_INCLUDE_DIRS})
else()
    message("-------Did not find Pangolin, cannot include dir!!!")
endif()

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} ${Pangolin_LIBRARIES})

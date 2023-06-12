# PangolinPointCloud
--------------------
PointCloudPangolin is a simple project to demonstrate creation and display of point clouds using the [Pangolin](https://github.com/stevenlovegrove/Pangolin) library. 
Pangolin is a lightweight library for easy visualization of 3D and video based data using OpenGL.
However, it lacks examples of rendering point cloud data.
This project attempts to fill in this gap and demonstates point cloud visualization using the Pangolin library.

## Features
-----------
- Creation of a point cloud
- Coloring of the point cloud
- Drawing the point cloud
- Adjusting the point size of the rendered point cloud

## Dependencies
---------------
- Pangolin

## Prerequisites
----------------
It is assumed that the following are installed and configured
- Compiler: Visual Studio C++
- Code editor: Visual Studio Code with C++ and CMake extensions
- Build system generator: CMake
- Version control: git 
- C++ dependency manager: vcpkg

## Installation
---------------
# Windows (Tested so far)
- Install Pangolin ([vcpkg package](https://vcpkg.io/en/packages.html)) using the command
```
vcpkg install pangolin:x64-windows
```
- Note the path where vcpkg is installed. Make sure to use the same path in the CMakeLists.txt inside the "PointCloudPangolin" folder
- Open the "PointCloudPangolin" folder in VS Code
- Build
- Run

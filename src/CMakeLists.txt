cmake_minimum_required(VERSION 2.8)
 
PROJECT(Cylinder)

SET(VTK_DIR C:/Users/dgrop/source/repos/VTK-bin)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})
 
add_executable(Cylinder MACOSX_BUNDLE Cylinder.cxx)
 
if(VTK_LIBRARIES)
  target_link_libraries(Cylinder ${VTK_LIBRARIES})
else()
  target_link_libraries(Cylinder vtkHybrid vtkWidgets)
endif()
cmake_minimum_required(VERSION 2.8)

PROJECT(SceneMountains)

find_package(GLUT REQUIRED)
include_directories(${GLUT_INCLUDE_DIRS})
link_directories(${GLUT_LIBRARY_DIRS})
add_definitions(${GLUT_DEFINITIONS})

find_package(OpenGL REQUIRED)
include_directories(${OpenGL_INCLUDE_DIRS})
link_directories(${OpenGL_LIBRARY_DIRS})
add_definitions(${OpenGL_DEFINITIONS})

add_executable(SceneMountains Camera.cpp Source.cpp)


target_link_libraries(SceneMountains ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} )
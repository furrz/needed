project(needed)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)

find_package(OpenGL)
find_package(GLEW)
find_package(glfw3 REQUIRED)

include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLEW_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS} )

add_executable(${PROJECT_NAME} ${SRC_LIST})

target_link_libraries(needed ${OPENGL_LIBRARIES} ${GLEW_LIBRARY} glfw)

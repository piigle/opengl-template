cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(template)

add_subdirectory("lib/glfw")
find_package(OpenGL REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR}/lib ${CMAKE_CURRENT_SOURCE_DIR}/include ${CMAKE_CURRENT_SOURCE_DIR}/lib/glm ${CMAKE_CURRENT_SOURCE_DIR}/lib/glfw/include)

add_executable(template src/shader.cpp src/main.cpp lib/glad/glad.c)

target_link_libraries(template PUBLIC ${OPENGL_LIBRARIES} glfw)
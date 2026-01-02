cmake_minimum_required(VERSION 3.31)
project(OpenGLLearn)

set(CMAKE_CXX_STANDARD 20)

include_directories(${PROJECT_SOURCE_DIR}/include)
include_directories(${PROJECT_SOURCE_DIR}/include/GLFW)
include_directories(${PROJECT_SOURCE_DIR}/include/glad)

link_directories(${PROJECT_SOURCE_DIR}/libs/mingw)

add_executable(${PROJECT_NAME}
        main.cpp
        ${PROJECT_SOURCE_DIR}/libs/mingw/glad.c      # 同样，请根据实际路径修改
)

target_link_libraries(${PROJECT_NAME} glfw3 opengl32 gdi32)

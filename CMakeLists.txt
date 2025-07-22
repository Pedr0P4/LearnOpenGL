cmake_minimum_required(VERSION 3.10)
project(LearnOpenGL)

add_executable(LearnOpenGL src/main.cpp)

# Headers do GLFW
target_include_directories(LearnOpenGL PRIVATE ${CMAKE_SOURCE_DIR}/include)

# Biblioteca compilada
target_link_libraries(LearnOpenGL PRIVATE ${CMAKE_SOURCE_DIR}/lib/libglfw3.a)

# Bibliotecas do sistema que o GLFW depende
target_link_libraries(LearnOpenGL PRIVATE opengl32 gdi32 user32)
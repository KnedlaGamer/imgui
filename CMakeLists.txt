cmake_minimum_required(VERSION 3.30)

project(ImGui)

set(CMAKE_CXX_STANDARD 23)

file(GLOB ImGuiSource "*.cpp" "*.h")

add_library(${PROJECT_NAME}
        ${ImGuiSource}
        backends/imgui_impl_glfw.cpp
        backends/imgui_impl_opengl3.cpp
)
target_include_directories(ImGui PUBLIC ./ ${LibDirectory}/glfw/include)
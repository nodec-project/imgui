cmake_minimum_required(VERSION 3.15)

project(imgui LANGUAGES CXX)

add_library(${PROJECT_NAME} STATIC
    imgui/imgui.cpp
    imgui/imgui_demo.cpp
    imgui/imgui_draw.cpp
    imgui/imgui_tables.cpp
    imgui/imgui_widgets.cpp
)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC imgui
)

target_compile_features(
    ${PROJECT_NAME} PUBLIC cxx_std_11
)

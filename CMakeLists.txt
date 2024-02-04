cmake_minimum_required(VERSION 3.12)

project(ImGui LANGUAGES CXX)

include_directories(./)

set(ImGuiFiles 
    imgui.cpp           # Essential files
    imgui_widgets.cpp 
    imgui_tables.cpp 
    imgui_draw.cpp 
    imgui_demo.cpp
                        # DirectX 3D/Win32 files
    backends/imgui_impl_dx10.cpp
    backends/imgui_impl_dx11.cpp
    backends/imgui_impl_dx12.cpp
    backends/imgui_impl_win32.cpp
    )

add_library(${PROJECT_NAME} ${ImGuiFiles})
target_include_directories(${PROJECT_NAME} INTERFACE ./)
project(imgui)

file(GLOB_RECURSE imgui_src "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

add_library(imgui STATIC ${imgui_src})

target_include_directories(imgui PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/backends
)

target_link_libraries(imgui PRIVATE SDL3)

# imgui.demo
add_executable(demo_imgui example.sdl3.sdlrenderer3.cpp)
target_link_libraries(demo_imgui PRIVATE imgui SDL3)
set_target_properties(demo_imgui PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}
)
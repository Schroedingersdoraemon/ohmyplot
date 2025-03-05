cmake_minimum_required(VERSION 3.10.0)
project(ohmyplot VERSION 0.1.0 LANGUAGES C CXX)

add_subdirectory(third_party/SDL3)
add_subdirectory(third_party/imgui)
add_subdirectory(third_party/implot)

add_executable(ohmyplot main.cpp)
target_link_libraries(ohmyplot imgui implot)


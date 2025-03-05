project(implot)

file(GLOB implot_src "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

add_library(implot STATIC ${implot_src})

target_include_directories(implot PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(implot PRIVATE imgui)
if(WIN32)

else()

    find_package(SDL3 REQUIRED CONFIG)

    add_library(SDL3 INTERFACE)
    target_include_directories(SDL3 INTERFACE ${SDL3_INCLUDE_DIRS})
    target_link_libraries(SDL3 INTERFACE ${SDL3_LIBRARIES})

endif()
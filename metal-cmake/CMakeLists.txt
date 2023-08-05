# Library definition
add_library(METAL_CPP
        ${CMAKE_CURRENT_SOURCE_DIR}/definition.cpp
        )

# Metal cpp headers
target_include_directories(METAL_CPP PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}/metal-cpp"
        "${CMAKE_CURRENT_SOURCE_DIR}/metal-cpp-extensions"
        )

# Metal cpp library (linker)
target_link_libraries(METAL_CPP
        "-framework Metal"
        "-framework MetalKit"
        "-framework AppKit"
        "-framework Foundation"
        "-framework QuartzCore"
        )

cmake_minimum_required(VERSION 3.21)
set(CMAKE_CXX_STANDARD 17)
project(metal_cpp_try)

# Add metal cmake definition
add_subdirectory(metal-cmake)
add_subdirectory(src)

file(GLOB SRC
        src/main.cpp
        )

add_executable(${PROJECT_NAME} ${SRC})

target_link_libraries(${PROJECT_NAME}
        METAL_CPP
        )

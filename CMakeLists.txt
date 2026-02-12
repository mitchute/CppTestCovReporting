cmake_minimum_required(VERSION 3.20)

project(HelloWorld
    VERSION 1.0
    LANGUAGES CXX
)

# Enforce modern C++
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(hello
    src/main.cpp
)

# Optional: stricter warnings (recommended)
if (MSVC)
    target_compile_options(hello PRIVATE /W4)
else()
    target_compile_options(hello PRIVATE -Wall -Wextra -Wpedantic)
endif()


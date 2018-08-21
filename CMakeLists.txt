cmake_minimum_required(VERSION 3.11)

project(vmls)

if (MSVC)
    add_compile_options(/W4 /WX)
else()
    add_compile_options(-Wall -Wextra -pedantic -Werror)
endif()

add_library(eigen INTERFACE)
target_include_directories(eigen INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/eigen-git-mirror)
target_compile_features(eigen INTERFACE cxx_std_14)

add_subdirectory(src)

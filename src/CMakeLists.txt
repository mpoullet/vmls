add_executable(vmls vmls.cpp)

set_target_properties(vmls PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED YES
    CXX_EXTENSIONS NO
)

target_link_libraries(vmls PRIVATE eigen)

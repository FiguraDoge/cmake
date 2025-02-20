add_executable(test_component main.cpp)
target_include_directories(test_component PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../../source/common
        ${CMAKE_CURRENT_SOURCE_DIR}/../../source/component
)

target_link_libraries(test_component PUBLIC common_static component_static)
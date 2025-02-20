add_library(common_obj OBJECT example_common.cpp)
target_include_directories(common_obj PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

add_library(common_static STATIC $<TARGET_OBJECTS:common_obj>)
add_library(common_shared SHARED $<TARGET_OBJECTS:common_obj>)
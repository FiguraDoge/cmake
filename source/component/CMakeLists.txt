add_library(component_obj OBJECT example_component.cpp)
target_include_directories(component_obj PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
        ${CMAKE_CURRENT_SOURCE_DIR}/../common
)
target_link_libraries(component_obj PUBLIC common_static)

add_library(component_static STATIC $<TARGET_OBJECTS:component_obj>)
add_library(component_shared SHARED $<TARGET_OBJECTS:component_obj>)
target_link_libraries(component_static PUBLIC common_static)        # my question here
target_link_libraries(component_shared PUBLIC common_static)        # my question here
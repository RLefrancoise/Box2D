project(box2d)

file(
        GLOB
        BOX2D_SOURCES
        RELATIVE
        ${CMAKE_CURRENT_SOURCE_DIR}
        "Box2D/**/*.h"
        "Box2D/**/*.cpp"
)

add_library(box2d STATIC ${BOX2D_SOURCES})
target_include_directories(box2d PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
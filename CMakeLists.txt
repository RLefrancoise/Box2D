project(box2d)

file(
        GLOB
        BOX2D_SOURCES
        RELATIVE
        ${CMAKE_CURRENT_SOURCE_DIR}
        "Box2D/Box2D.h"
        "Box2D/Collision/*.h"
        "Box2D/Collision/*.cpp"
        "Box2D/Collision/Shapes/*.h"
        "Box2D/Collision/Shapes/*.cpp"
        "Box2D/Common/*.h"
        "Box2D/Common/*.cpp"
        "Box2D/Dynamics/*.h"
        "Box2D/Dynamics/*.cpp"
        "Box2D/Dynamics/Contacts/*.h"
        "Box2D/Dynamics/Contacts/*.cpp"
        "Box2D/Dynamics/Joints/*.h"
        "Box2D/Dynamics/Joints/*.cpp"
        "Box2D/Rope/*.h"
        "Box2D/Rope/*.cpp"
)

add_library(box2d STATIC ${BOX2D_SOURCES})
target_include_directories(box2d PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
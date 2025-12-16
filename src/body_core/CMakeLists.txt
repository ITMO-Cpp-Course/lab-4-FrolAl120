add_library(body_core STATIC
        src/body.cpp
)

target_link_libraries(body_core PRIVATE project_warnings)
if (TARGET project_sanitizers)
        target_link_libraries(body_core PRIVATE project_sanitizers)
endif ()

target_include_directories(body_core
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)


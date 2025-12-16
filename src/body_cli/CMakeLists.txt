add_executable(body_cli
        src/main.cpp
)

target_link_libraries(body_cli PRIVATE body_core project_warnings)
if (TARGET project_sanitizers)
        target_link_libraries(body_cli PRIVATE project_sanitizers)
endif ()


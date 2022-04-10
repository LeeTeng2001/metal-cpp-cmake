# Get all project dir
FILE(GLOB sample_projects ${CMAKE_CURRENT_SOURCE_DIR}/learn-metal/*)

# For each project dir, build a target
FOREACH(project ${sample_projects})
    IF(IS_DIRECTORY ${project})
        # Get project name and all sources
        get_filename_component(project-name ${project} NAME)
        FILE(GLOB ${project}-src ${project}/*.cpp)

        # Create executable and link target
        add_executable(${project-name} ${${project}-src})
        target_link_libraries(${project-name} METAL_CPP)

        message(STATUS "Adding ${project-name}")
    ENDIF()
ENDFOREACH()

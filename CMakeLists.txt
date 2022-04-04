cmake_minimum_required(VERSION 3.16)
project(hardware-documentation VERSION 1.0.0)
set(CMAKE_EXPORT_COMPILE_COMMANDS TRUE)

# C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


# Check for xenomai as these drivers are xenomai compatible.

# message(STATUS "Create compile commands.")
# execute_process(
#     COMMAND ln -s "${PROJECT_BINARY_DIR}/compile_commands.json" "${PROJECT_SOURCE_DIR}/compile_commands.json"
#     ERROR_QUIET
# )

add_custom_target(build-hardware-documentation ALL
  COMMAND ${CMAKE_COMMAND} -E copy_directory
  ${CMAKE_CURRENT_SOURCE_DIR}/docs ${CMAKE_CURRENT_BINARY_DIR}/docs
  COMMENT "Moving docs into build directory ${CMAKE_CURRENT_BINARY_DIR}..."
)

message(STATUS "Cmake install to: ${CMAKE_INSTALL_PREFIX}/docs")

install(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/docs" DESTINATION "${CMAKE_INSTALL_PREFIX}/docs")

# install(DIRECTORY "./docs")

# option(BUILD_DOCS "Enable the configuration and building of the documentation." FALSE)
# option(BUILD_DOCS_SUPERBUILD "Build the docs with the purpose of using in the superbuild doc compilation. \
# This will make it so the docs are not built only configured." FALSE)
#
# IF(BUILD_DOCS)
#     add_subdirectory(docs)
# ENDIF()

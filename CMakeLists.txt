cmake_minimum_required(VERSION 3.16)
project(hardware-documentation VERSION 1.0.0)

add_executable(dummy-target "${CMAKE_CURRENT_SOURCE_DIR}/cmake/dummy.cpp")

add_custom_target(build-hardware-documentation ALL DEPENDS dummy-target
  COMMAND ${CMAKE_COMMAND} -E copy_directory
  ${CMAKE_CURRENT_SOURCE_DIR}/docs ${CMAKE_CURRENT_BINARY_DIR}/docs
  COMMENT "Moving docs into build directory ${CMAKE_CURRENT_BINARY_DIR}..."
)

install(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/docs" DESTINATION "${CMAKE_INSTALL_PREFIX}/docs")



# # set(FAKE_TARGET build-hardware-documentation)
# add_custom_target(TARGET ${PROJECT_NAME} ALL PRE_BUILD
#   COMMAND ${CMAKE_COMMAND} -E copy_directory
#   ${CMAKE_CURRENT_SOURCE_DIR}/docs ${CMAKE_CURRENT_BINARY_DIR}/docs
#   COMMENT "Moving docs into build directory ${CMAKE_CURRENT_BINARY_DIR}..."
# )
# # add_dependencies(${PROJECT_NAME} ${FAKE_TARGET})
#
# install(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/docs" DESTINATION "${CMAKE_INSTALL_PREFIX}/docs")

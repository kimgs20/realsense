cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamplesHelloRealSense)

add_executable(rs-hello-realsense rs-hello-realsense.cpp)
set_property(TARGET rs-hello-realsense PROPERTY CXX_STANDARD 11)
# target_link_libraries(rs-hello-realsense ${DEPENDENCIES})  // set(DEPENDENCIES realsense2) at root dir
target_link_libraries(rs-hello-realsense realsense2)
set_target_properties (rs-hello-realsense PROPERTIES FOLDER "Examples")

install(TARGETS rs-hello-realsense RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
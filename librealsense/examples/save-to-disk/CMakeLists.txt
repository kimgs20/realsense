cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamplesSaveToDisk)

add_executable(rs-save-to-disk rs-save-to-disk.cpp)
set_property(TARGET rs-save-to-disk PROPERTY CXX_STANDARD 11)
target_link_libraries(rs-save-to-disk ${DEPENDENCIES})
include_directories(../../common ../../third-party ../../third-party/tclap/include)
set_target_properties (rs-save-to-disk PROPERTIES FOLDER "Examples")
install(TARGETS rs-save-to-disk RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})

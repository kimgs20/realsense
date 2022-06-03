cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamplesCapture)

# problem with gl
# /usr/bin/ld: rs-capture.cpp:(.text+0xdc3): undefined reference to `glLoadIdentity'
# /usr/bin/ld: rs-capture.cpp:(.text+0xdcd): undefined reference to `glMatrixMode'
# /usr/bin/ld: rs-capture.cpp:(.text+0xe14): undefined reference to `glOrtho'
if(BUILD_GRAPHICAL_EXAMPLES)
    add_executable(rs-capture rs-capture.cpp ../example.hpp)
    set_property(TARGET rs-capture PROPERTY CXX_STANDARD 11)
    target_link_libraries(rs-capture realsense2)
    include_directories(../ ../../third-party/tclap/include ../../examples)
    set_target_properties (rs-capture PROPERTIES FOLDER "Examples")

    install(TARGETS rs-capture RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
endif()

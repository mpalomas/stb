
set(INCLUDES "${CMAKE_CURRENT_SOURCE_DIR}")

add_library(stb INTERFACE)
add_library(stb::stb ALIAS stb)
target_include_directories(stb
        INTERFACE
            $<BUILD_INTERFACE:${INCLUDES}>
            $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>)

cmake_minimum_required(VERSION 3.1)

project(SFMLTest)

## If you want to link SFML statically
#set(SFML_STATIC_LIBRARIES TRUE)

## In most cases better set in the CMake cache
#set(SFML_DIR "./external/SFML-2.5.1-windows-mingw-64-bit/lib/cmake/SFML")

## or to build from source files
add_subdirectory(external/SFML-2.5.1-sources)

## use find if not building from source
#find_package(SFML 2.5 COMPONENTS graphics audio REQUIRED)
add_executable(SFMLTest main.cpp)
target_link_libraries(SFMLTest sfml-graphics sfml-audio)

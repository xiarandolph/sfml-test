cmake_minimum_required(VERSION 3.1)

project(SFMLTest)

## If you want to link SFML statically
set(SFML_STATIC_LIBRARIES TRUE)

## In most cases better set in the CMake cache
#set(SFML_DIR "<sfml root directorty>/lib/cmake/SFML")

add_subdirectory(external/SFML-2.5.1)

#find_package(SFML 2.5 COMPONENTS graphics audio REQUIRED)
add_executable(SFMLTest main.cpp)
target_link_libraries(SFMLTest sfml-graphics sfml-audio)

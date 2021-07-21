cmake_minimum_required(VERSION 3.10)

# set the project name
project("Rogue Fairy Studios - Storyteller Tools" VERSION 0.1)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# General Include
include_directories("${PROJECT_SOURCE_DIR}/include")

# SDL
# Add SDL Stuff

# add the executable
add_executable(StoryTeller storyteller.cpp)

target_link_libraries(StoryTeller ${SDL2_LIBRARY})    

target_include_directories(StoryTeller PUBLIC
                          "${SDL2_INCLUDE_DIR}"
                          "${PROJECT_SOURCE_DIR}/thirdparty/imgui/"
                          "${PROJECT_SOURCE_DIR}/thirdparty/imgui/backends/"
                          "${PROJECT_SOURCE_DIR}/thirdparty/imgui/libs/"
                          "${PROJECT_SOURCE_DIR}/thirdparty/SDL/include/"
                          "${PROJECT_SOURCE_DIR}/thirdparty/SDL/VisualC/SDL/")
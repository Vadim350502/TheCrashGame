cmake_minimum_required (VERSION 3.8)

project(engine)

set(CMAKE_CXX_STANDART 17)

add_library(engineLib STATIC "src/Engine.hpp" "src/Engine.cpp" )

if(NOT IOS)
	add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/Libs/SDL2)
	set(${SDL2MAIN_LIBRARY} SDL2main)
	set(${SDL2_LIBRARY} SDL2-static)
endif()

target_include_directories(engineLib  PUBLIC
${CMAKE_CURRENT_SOURCE_DIR}/src 
${CMAKE_CURRENT_SOURCE_DIR}/Libs/SDL2/include
)
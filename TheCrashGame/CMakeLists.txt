# CMakeList.txt : CMake project for TheCrashGame, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

project(TheCrashGame)

set(CMAKE_CXX_STANDART 17)

add_subdirectory(engine)

add_executable(TheCrash "src/GameInit.cpp")

target_link_libraries(engineLib PRIVATE ${SDL2MAIN_LIBRARY} ${SDL2_LIBRARY})

# Add source to this project's executable.
#add_executable (TheCrashGame  "TheCrashGame.h")

# TODO: Add tests and install targets if needed.

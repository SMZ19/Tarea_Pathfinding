cmake_minimum_required(VERSION 3.14)
project(pathfinding)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES knight.cpp knight.h main.cpp crusader.cpp crusader.h Bresenham.cpp Bresenham.h)
# Include a library search using find_package()
# via REQUIRED, specify that libraries are required
find_package(Qt5Core REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Widgets REQUIRED)

add_executable(pathfinding ${SOURCE_FILES})

# specify which libraries to connect
target_link_libraries(${PROJECT_NAME} Qt5::Core)
target_link_libraries(${PROJECT_NAME} Qt5::Gui)
target_link_libraries(pathfinding Qt5::Widgets)


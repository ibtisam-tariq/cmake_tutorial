cmake_minimum_required(VERSION 2.8)
project(Tutorial_Project)

# Adding compiler flags (see using make VERBOSE=1)
set(CMAKE_CXX_FLAGS "-std=c++0x -Wall")
# or 
# add_definitions(-Wall -std=c++0x)

# add subdirectory
add_subdirectory(src)

#Show output on terminal during cmake command
message("${CMAKE_CURRENT_SOURCE_DIR} , ${PROJECT_SOURCE_DIR}, ${PROJECT_BINARY_DIR}")
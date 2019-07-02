#Change this if you need to target a specific CMake version
cmake_minimum_required(VERSION 2.6)
project(sdlopengltest)

# Enable debug symbols by default
if(CMAKE_BUILD_TYPE STREQUAL "")
  set(CMAKE_BUILD_TYPE Debug)
endif()
# (you can also set it on the command line: -D CMAKE_BUILD_TYPE=Debug)

include_directories("${PROJECT_BINARY_DIR}") 
include_directories("${CMAKE_CURRENT_SOURCE_DIR}")

# Define sources and executable
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -Wall -Wextra -pedantic -lSDL2")
set(EXECUTABLE_NAME "sdlopengltest")
set(MY_SOURCES 
   
   )

add_executable(${EXECUTABLE_NAME} ${MY_SOURCES})

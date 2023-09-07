cmake_minimum_required(VERSION 3.22.1)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include(GNUInstallDirs)

project(platon_workflows VERSION 1.0)
file(GLOB_RECURSE SRC_FILES src/*.cxx)
file (GLOB_RECURSE HEADERS CONFIGURE_DEPENDS include/*.hxx )
add_library(${PROJECT_NAME} SHARED ${SRC_FILES})

target_include_directories(${PROJECT_NAME}
  PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
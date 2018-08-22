cmake_minimum_required(VERSION 3.10)
project(wco)

set(CMAKE_CXX_STANDARD 14)

if(EXISTS ${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    conan_basic_setup()
else()
    message(WARNING "The file conanbuildinfo.cmake doesn't exist, you have to run conan install first")
endif()

add_executable(wco main.cpp)
target_link_libraries(wco ${CONAN_LIBS})
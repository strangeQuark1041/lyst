cmake_minimum_required(VERSION 3.22.1)
project(lyst LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include(FetchContent)
FetchContent_Declare(
  fmt
  GIT_REPOSITORY https://github.com/fmtlib/fmt.git
  GIT_TAG        09fde7f4b86c21005121bea7ea9bbe39096294e5 # release-8.1.1
)
FetchContent_MakeAvailable(fmt)

add_executable(lyst main.cpp)

target_compile_options(
    lyst PRIVATE 
)

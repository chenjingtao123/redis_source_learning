
cmake_minimum_required(VERSION 2.8)
project(redis_source_learning)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_USE_RELATIVE_PATHS ON)
include_directories(${PROJECT_SOURCE_DIR}/src)
include_directories(${PROJECT_SOURCE_DIR}/deps/lua/src)
include_directories(${PROJECT_SOURCE_DIR}/deps/hiredis)

aux_source_directory(${PROJECT_SOURCE_DIR}/src SOURCE_FILES)
aux_source_directory(${PROJECT_SOURCE_DIR}/deps/lua/src SOURCE_FILES)
aux_source_directory(${PROJECT_SOURCE_DIR}/deps/hiredis SOURCE_FILES)

add_executable(redis_source_learning ${SOURCE_FILES})





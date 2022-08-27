cmake_minimum_required(VERSION 3.24.0)

file(GLOB_RECURSE SRC_FILES ./*.c)
add_library(Zeus STATIC ${SRC_FILES})

target_include_directories(Zeus
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../include
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(Zeus glad)

cmake_minimum_required(VERSION 3.20.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXE_LINKER_FLAGS "-no-pie")

project(SampleLibevent VERSION 1.0.0 LANGUAGES CXX C)

# Include
include_directories()

# Link
link_directories()

# Source code
file(GLOB SRC)

# RealGame
add_executable(${PROJECT_NAME} ${SRC} src/main.cpp )
target_link_libraries(${PROJECT_NAME})

add_custom_target(run ${PROJECT_NAME}
	DEPENDS ${SAMPLE}
    WORKING_DIRECTORY ${PROJECT_SOURCE_DIR})

cmake_minimum_required(VERSION 3.26.4)

project(cppscratch)

# Fix missing link directories on macos (when using default locations)
# Has to be placed before add_executable and target_link_libraries
#link_directories(/usr/local/lib)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(adder)

# target_link_directories required only if library and headers are not installed in default locations
#target_link_directories(${PROJECT_NAME} PRIVATE ${CMAKE_SOURCE_DIR}/adder/build/)
target_link_libraries(${PROJECT_NAME} adder)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)

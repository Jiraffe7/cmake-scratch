cmake_minimum_required(VERSION 3.26.4)

project(adder)

add_library(${PROJECT_NAME} adder.cpp)

# for installing library into /usr/local/lib and
# library headers in include /usr/local/include
set_target_properties(${PROJECT_NAME} PROPERTIES PUBLIC_HEADER adder.h)
install(TARGETS ${PROJECT_NAME} LIBRARY DESTINATION lib
	PUBLIC_HEADER DESTINATION include
	)

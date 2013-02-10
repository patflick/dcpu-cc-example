cmake_minimum_required(VERSION 2.8.5)
project(dcpu-cc-example)

# add the compiler subdirectory
add_subdirectory(libdcpu-cc)

# add the compiler dir as include dir
include_directories(
    ${libdcpu-cc_SOURCE_DIR}
)

# build an executable from main
add_executable(dcpu-cc-example
	main.cpp
)

# link the executable with the library
target_link_libraries(dcpu-cc-example
	libdcpu-cc
)

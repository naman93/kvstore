#add all source files
set (network_source_files
	nw_config.h
	server.c
	server.h
	client.c
	client.h
	network.c
	network.h
)

#indicate where the library files need to be put
set(LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/obj)
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/obj)

#include directories
include_directories(../transaction ../storage)

#add as a library
add_library(network STATIC ${network_source_files})

#add link libraries
target_link_libraries(network transaction storage)

#add all source files
set (storage_source_files
	storage.c
	storage.h
)

#indicate where the library files need to be put
set(LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/obj)
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/obj)

#add as a library
add_library(storage STATIC ${storage_source_files})

add_library(print_library SHARED print_lib.cpp)
set_target_properties(print_library PROPERTIES LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)

# for static libraries
# add_library(print_library STATIC print_lib.cpp)
# set_target_properties(print_library PROPERTIES ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)
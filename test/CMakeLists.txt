link_directories(${CMAKE_SOURCE_DIR}/lib)
include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(test_print test.cpp)
target_link_libraries(test_print "libprint_library.so")

set_target_properties(test_print PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)


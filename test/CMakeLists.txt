add_executable(test_print test.cpp)

# used by linker
target_link_directories(test_print PUBLIC ${CMAKE_SOURCE_DIR}/lib)
#used by compiler
target_include_directories(test_print PUBLIC ${CMAKE_SOURCE_DIR}/src)

target_link_libraries(test_print "libprint_library.so")

set_target_properties(test_print PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

#PUBLIC doesn't mean much for an executable; for a library it lets CMake know that any targets that link to this target must also need that include directory. Other options are PRIVATE (only affect the current target, not dependencies), and INTERFACE (only needed for dependencies).
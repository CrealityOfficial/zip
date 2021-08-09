file(GLOB ZIP_SRC *.c)

__add_real_target(zip lib SOURCE ${ZIP_SRC} LIB zlib INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
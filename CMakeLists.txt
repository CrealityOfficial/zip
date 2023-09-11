file(GLOB ZIP_SRC *.c)

__cc_find(zlib_static)
__add_real_target(zip_static lib SOURCE ${ZIP_SRC} 
						  LIB zlib_static
						  INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
					    )

if(CC_INSTALL_ZIP_STATIC)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/ zip_static)
endif()

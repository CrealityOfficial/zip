file(GLOB ZIP_SRC *.c)
set(DEFS Z_PREFIX)

__add_real_target(zip lib SOURCE ${ZIP_SRC} LIB zlib
					    DEF ${DEFS}
					    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
					    )

if(CC_INSTALL_ZIP)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/ zip)
endif()

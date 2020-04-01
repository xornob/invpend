cmake_minimum_required(VERSION 3.13)
project(InvPend)

option( INVPEND_ENABLE_SAMPLES "Compile samples if true." TRUE )
option( INVPEND_ENABLE_CLIENT "Compile client if true." TRUE )
option( INVPEND_ENABLE_SERVER "Compile server if true." TRUE )

set( INVPED_HEADER_DIR ${InvPend_SOURCE_DIR}/lib )

add_subdirectory(lib)

if( INVPEND_ENABLE_SAMPLES )
	add_subdirectory(samples)
endif()

if( INVPEND_ENABLE_CLIENT )
	add_subdirectory(client)
endif()

if( INVPEND_ENABLE_SERVER )
	add_subdirectory(server)
endif()

cmake_minimum_required(VERSION 3.13)

option(IPLIB_SAMPLE_hello_udp "" True)

if(IPLIB_SAMPLE_hello_udp)
	add_subdirectory("hello_udp")
endif()

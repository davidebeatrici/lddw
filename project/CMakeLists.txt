cmake_minimum_required(VERSION 3.18.4)

project(lddw
	VERSION "0.1.0"
	DESCRIPTION "An ldd (List Dynamic Dependencies) implementation for Windows."
	HOMEPAGE_URL "https://github.com/Sharp0802/lddw"
	LANGUAGES "C"
)

set(CMAKE_C_EXTENSIONS OFF)
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_VISIBILITY_PRESET hidden)

set(INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/inc")

if(MSVC)
	add_compile_options(
		"/W4"
		"/WX"
	)
else()
	add_compile_options(
		"-pedantic"
		"-Wall"
		"-Wextra"
	)
endif()

add_subdirectory(src)

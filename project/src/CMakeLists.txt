add_executable(lddw
	"main.c"

	"dict.c"
	"ldd.c"
	"log.c"
)

target_compile_definitions(lddw
	PRIVATE
		"_UNICODE"
		"UNICODE"
)

target_include_directories(lddw
	PRIVATE
		${INCLUDE_DIR}
)

set_target_properties(lddw PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}
)

add_library(
	a
	STATIC
	src.cpp
)

# these headers will be exposed ONLY to "a" library
target_include_directories(
	a
	PRIVATE
	priv
)

# these headers will be passed on during target_link_libraries
target_include_directories(
	a
	PUBLIC
	include
)

# this is a private compile option
target_compile_options(
	a
	PRIVATE
	-DTHIS_IS_PRIVATE
)

# this is a public compile option, it will be passed on during target_link_libraries
target_compile_options(
	a
	PUBLIC
	-DTHIS_IS_PUBLIC
)

# we hide our dependencies here
add_library(
    b1
    SHARED
    src.cpp
)
# these headers will be passed on during target_link_libraries
target_include_directories(
    b1
    PUBLIC
    include
)
# these libraries will be exposed ONLY to "b1" library
target_link_libraries(
    b1
    PRIVATE
    a
)

# we expose our dependencies here
add_library(
    b2
    SHARED
    src.cpp
)
# these headers will be passed on during target_link_libraries
target_include_directories(
    b2
    PUBLIC
    include
)
# these libraries will be passed on during target_link_libraries
target_link_libraries(
    b2
    PUBLIC
    a
)

# expose dependencies ONLY when their API is visible in "PUBLIC" headers
# ie. when you use cv::Mat in PUBLIC headers, link opencv as public (or at least opencv_core)

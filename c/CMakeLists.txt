
add_executable(
    test1
    src1.cpp
)
# "test1" can use only "b" headers, since "a" is declared PRIVATE when building "b1"
target_link_libraries(
    test1
    b1
)

add_executable(
    test2
    src2.cpp
)
# "test2" can use "a" and "b" headers, since "a" is declared PUBLIC when building "b1"
target_link_libraries(
    test2
    b2
)

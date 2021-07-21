cmake_minimum_required(VERSION 3.14)
project(example)

# use switches to persist configuration options, ie. compile static or dynamic, enable some feature etc.
# see doc https://cmake.org/cmake/help/latest/command/option.html
option(example_switch "THis is an example switch, default ON" ON)

add_subdirectory(a)
add_subdirectory(b)
add_subdirectory(c)


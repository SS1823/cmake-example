# CMake project sample

dependency chain
* a -> b1 -> test1 (does not see a headers or defines)
* a -> b2 -> test2 (sees a headers and defines)

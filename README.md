# CMake project sample

dependency chain
* a -> b1 -> test1 (does not see a headers or defines)
* a -> b2 -> test2 (sees a headers and defines)

# Building

Switch use is optional (the `-Dexample_switch=XXX`)

Windows:
* `mkdir build`
* `cmake -B build -Dexample_switch=OFF`
* `cmake --build build --config RelWithDebInfo`

Linux:
* `mkdir build`
* `cmake -B build -Dexample_switch=OFF -DCMAKE_BUILD_TYPE=RelWithDebInfo`
* `cmake --build build`


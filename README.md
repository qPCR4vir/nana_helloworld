# nana_helloworld
A full Hello World nana example.
I added the cmake options:


```
-DCMAKE_INSTALL_PREFIX="../"
-DNANA_CMAKE_NANA_FILESYSTEM_FORCE=OFF
-DNANA_CMAKE_INSTALL_INCLUDES=OFF
-DNANA_CMAKE_ENABLE_JPEG=ON
-DNANA_CMAKE_ENABLE_PNG=ON
-DJPEG_HAVE_BOOLEAN=ON
-DNANA_CMAKE_AUTOMATIC_GUI_TESTING=OFF
```

In CLion they are added in menu File/Settings... /Builds, Execution.../Cmake/Cmake options:

I also set:

in menu File/Settings... /Builds, Execution.../Cmake/Generating Paths:

```
..\cmake-nana-hello-build-debug
```

this will call:

```
"C:\Program Files\CMake\bin\cmake.exe" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../ -DNANA_CMAKE_NANA_FILESYSTEM_FORCE=OFF -DNANA_CMAKE_INSTALL_INCLUDES=OFF -DNANA_CMAKE_ENABLE_JPEG=ON -DNANA_CMAKE_ENABLE_PNG=ON -DJPEG_HAVE_BOOLEAN=ON -DNANA_CMAKE_AUTOMATIC_GUI_TESTING=OFF -G "CodeBlocks - MinGW Makefiles" C:\Prog\ExtLib\nana_helloworld
```

and upon "install" will produce:

```
...
-- Build files have been written to: C:/Prog/ExtLib/cmake-nana-hello-build-debug
[ 97%] Built target nana
Scanning dependencies of target nana_helloworld
[ 98%] Building CXX object CMakeFiles/nana_helloworld.dir/helloworld_demo.cpp.obj
[100%] Linking CXX executable nana_helloworld.exe
[100%] Built target nana_helloworld
Install the project...
-- Install configuration: "Debug"
-- Installing: C:/Prog/ExtLib/bin/nana_helloworld/nana_helloworld.exe

Install finished
```

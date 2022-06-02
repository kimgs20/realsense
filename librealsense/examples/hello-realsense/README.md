# rs-hello-realsense

1. write `rs-hello-realsense.cpp` file

2. write `CMakeLists.txt` file

3. make dir and run make
```
$ mkdir build && cd build
$ cmake ..
$ make
```

4. run excutable in build directory
   
(option: build in terminal)
$ g++ -o rs-hello-realsense rs-hello-realsense.cpp -lrealsense2
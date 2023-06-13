# cmake cpp scratch project
Learning from this [youtube playlist](https://www.youtube.com/playlist?list=PLalVdRk2RC6o5GHu618ARWh0VO0bFlif4)

## Build makefiles
In the root directory, run the following command:
```
cmake -S . -B build --install-prefix ~/cpp/
```

-S to specify the directory where root CMakeLists.txt is located.
-B to specify where to output generated makefiles.
--install-prefix to specify where to install compiled binaries

## Install the compiled binary
In the directory of the generated makefile, run the following command:
```
make install
```

Otherwise specify the directory of the generated makefile
```
make -C build install
```

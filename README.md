# OpenCL-CTS-guide

### Getting the Source Code and Building

* Follow https://github.com/THU-DSP-LAB/llvm-project/blob/main/README.md
* Then, like
```
 git clone https://github.com/KhronosGroup/OpenCL-CTS.git

 mkdir OpenCL-CTS/build
 cmake -S OpenCL-CTS -B OpenCL-CTS/build \
       -DCL_INCLUDE_DIR=/path-to-install/include \
       -DCL_LIB_DIR=/path-to-install \
       -DOPENCL_LIBRARIES=/path-to-install/lib/libOpenCL.so

 cmake --build OpenCL-CTS/build --config Release
```
 
### Running the CTS

* Import environment variables, like
```
export CL_ICD_FILENAMES=/path-to-install/lib/libpocl.so
```
* Execute the test binary.
For example,
```
cd build/test_conformance/compiler
./test_compiler       ---  run all tests under the compiler
./test_compiler load_program_source    ---  Run the use case named load_program_source under the compiler
```
note: run "./test_compiler --help" to get the names of cases.

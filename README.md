# OpenCL-CTS-guide

### Getting the Source Code and Building

* Follow https://github.com/THU-DSP-LAB/llvm-project/blob/main/README.md
* Then, like
```
 git clone https://github.com/KhronosGroup/OpenCL-CTS.git  --- you need reset b57445e [NFC] README.md: fix typos (#1704)

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

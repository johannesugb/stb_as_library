# stb_as_library

Some of Sean T. Barrett's (stb) libraries put into a Visual Studio library project        
Original source and credits: [stb single-file public domain libraries for C/C++ by Sean T. Barrett](https://github.com/nothings/stb)

The pre-configured Visual Studio 2019 project builds `.lib` and `.dll` files for the following stb files:
* `stb_image.h`
* `stb_image_resize.h`
* `stb_image_write.h`
* `stb_dxt.h`
* `stb_perlin.h`

Changes to the orignal files:         
* functions are declared as `__declspec(dllexport)` when included as header
* functions are declared as `__declspec(dllimport)` when included as source (i.e. when the respective `*_IMPLEMENTATION` symbol is defined)

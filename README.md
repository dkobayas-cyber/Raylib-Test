# Raylib-Test

This is a minimum example of Raylib-based C programes based on a tutorial by Rudy Faile (https://www.youtube.com/watch?v=HPDLTQ4J_zQ)

Environment setup
---
- raylib

  Download `raylib-4.2.0_win64_mingw-w64.zip` and install by `raylib_installer_v4.2.mingw.exe` in https://github.com/raysan5/raylib/releases/tag/4.2.0 
- Path

  On Windows, navigate to "Edit the system enviromental variables" > "Advanced" tab > "Environment Variables...". Add the followings to the path: 
  - `C:\raylib\w64devkit\bin`
  - `C:\raylib\raylib\src`
- C compiler 

  Use `C:\raylib\w64devkit\bin\gcc.exe` that comes with the installation of raylib. Make sure to:  
  - Remove/unistall `gcc.exe` in other directories if you have one. 
  - Install the 64-bit version (this is a default version if you install `raylib-4.2.0_win64_mingw-w64.zip`)
  
- Build raylib 

  Navigate to `C:\raylib\raylib\examples\` folder on Command Prompt and type: 
  `mingw32-make PLATFORM=PLATFORM_DESKTOP`
  The build is successful if you get `"raylib static library generated (librarylib.a) in ../src!"` You now have a `librarlib.a` in a `..\src\` directory.
  
- Required files

  - Make `include` direcotry and copy/paste `raylib.h` file. 
  - Make `lib` direcotry and copy/paste `librarlib.a` file. 

Example programs
--- 
Example programs are found in `raylib\raylib\example\core\`
  
Compilation 
---
On the terminal in VS Code, you type the following: 
```
gcc [CODE_NAME].c -o [OUTPUT_NAME].exe  -O1 -Wall -std=c99 -Wno-missing-braces -I include/ -L lib/ -lraylib -lopengl32 -lgdi32 -lwinmm
```
If the compilation is successful, `[OUTPUT_NAME].exe` will be created. 

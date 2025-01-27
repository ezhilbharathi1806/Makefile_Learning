# Makefile_Learning
Important Links
- https://makefiletutorial.com/
- https://github.com/franneck94/UdemyMakefile

Here is a comprehensive list of **`gcc`** and **`g++`** command-line options and commands commonly used for compiling and linking programs in C and C++:

---

### **General Commands**
- **`gcc`**: GNU Compiler Collection for C.
- **`g++`**: GNU Compiler Collection for C++.

---

### **Basic Usage**
- **Compile only**:
  - `gcc -c file.c`: Compiles `file.c` into an object file (`file.o`).
  - `g++ -c file.cpp`: Compiles `file.cpp` into an object file.

- **Link and compile**:
  - `gcc file.c -o output`: Compiles and links `file.c`, creating the executable `output`.
  - `g++ file.cpp -o output`: Compiles and links `file.cpp`, creating the executable `output`.

---

### **Optimization Levels**
- `-O0`: No optimization (default).
- `-O1`: Optimize for code size and execution time.
- `-O2`: Further optimizations without space-speed trade-offs.
- `-O3`: Maximize performance at the cost of increased binary size.
- `-Ofast`: Enables all `-O3` optimizations and some unsafe ones.
- `-Os`: Optimize for size.
- `-Og`: Optimize for debugging experience.

---

### **Debugging**
- `-g`: Generate debugging information for use with tools like `gdb`.

---

### **Standard Selection**
- `-std=c99`: Use the C99 standard.
- `-std=c11`: Use the C11 standard.
- `-std=c++11`: Use the C++11 standard.
- `-std=c++17`: Use the C++17 standard.
- `-std=c++20`: Use the C++20 standard.

---

### **Warnings**
- `-Wall`: Enable all common warnings.
- `-Wextra`: Enable extra warnings.
- `-Werror`: Treat warnings as errors.
- `-pedantic`: Enforce strict compliance with standards.

---

### **Include Paths**
- `-I<path>`: Add `<path>` to the list of directories to search for header files.

---

### **Linking**
- `-L<path>`: Add `<path>` to the library search path.
- `-l<name>`: Link with library `lib<name>.so` or `lib<name>.a`.

---

### **Preprocessor Options**
- `-D<macro>`: Define a macro.
- `-U<macro>`: Undefine a macro.
- `-E`: Run the preprocessor only.

---

### **Output Options**
- `-o <file>`: Specify the name of the output file.
- `-M`: Generate makefile dependencies.

---

### **Advanced Flags**
- `-pthread`: Enable multithreading with POSIX threads.
- `-fPIC`: Generate position-independent code (useful for shared libraries).
- `-shared`: Create a shared library.
- `-static`: Create a statically linked binary.
- `-fno-exceptions`: Disable exception handling in C++.
- `-fno-rtti`: Disable runtime type information in C++.

---

### **Profiling and Analysis**
- `-pg`: Enable profiling with `gprof`.
- `-fprofile-generate`: Instrument the program for profiling.
- `-fprofile-use`: Use profiling information for optimization.

---

### **Cross-Compilation**
- `--target=<arch>`: Specify the target architecture.
- `-march=<arch>`: Generate code for a specific CPU architecture.

---

### **Examples**
1. **Compile a single C file**:
   ```bash
   gcc -o myprogram myprogram.c
   ```
2. **Compile with optimizations**:
   ```bash
   g++ -O2 -o optimized_program program.cpp
   ```
3. **Debugging build**:
   ```bash
   gcc -g -o debug_program debug_program.c
   ```
---
### **Convert object file to hex files**
  ```bash
  gcc -c your_program.c -o your_program.o
  objcopy -O ihex your_program.o your_program.hex
  ```

## ** gcc flags**

#### **Compilation and Linking Flags**

| Flag                | Meaning                                                                |
| ------------------- | ---------------------------------------------------------------------- |
| `-c`                | Compile source files to object files only (`.o`), no linking.          |
| `-o <file>`         | Specify the name of the output file (executable or object file).       |
| `-Wall`             | Enable **all important warnings**. Strongly recommended.               |
| `-Wextra`           | Enable extra warning messages beyond `-Wall`.                          |
| `-Werror`           | Treat all warnings as **errors**.                                      |
| `-g`                | Include debug info (for use with gdb debugger).                        |
| `-O0`               | No optimization (default). Good for debugging.                         |
| `-O1`, `-O2`, `-O3` | Optimization levels: higher numbers = more aggressive optimizations.   |
| `-Ofast`            | Enable all `-O3` optimizations + unsafe ones that may break standards. |
| `-Og`               | Optimize for debugging (balance between `-O0` and `-O1`).              |
| `-std=c99`          | Use C99 standard (can be `c89`, `c11`, `gnu99`, etc.).                 |
| `-I<dir>`           | Add directory to the list of directories to search for header files.   |
| `-L<dir>`           | Add directory to the library search path.                              |
| `-l<lib>`           | Link with library `lib<lib>.so` or `lib<lib>.a`.                       |
| `-static`           | Link statically (no dynamic libraries).                                |
| `-shared`           | Produce a shared library (`.so` file).                                 |

#### **Debugging and Analysis**

| Flag                   | Meaning                                                   |
| ---------------------- | --------------------------------------------------------- |
| `-g`                   | Generate debug information.                               |
| `-pg`                  | Enable profiling for use with `gprof`.                    |
| `-fsanitize=address`   | Enable AddressSanitizer (runtime memory error detection). |
| `-fsanitize=undefined` | Detect undefined behavior at runtime.                     |

#### **Preprocessing**

| Flag        | Meaning                                       |
| ----------- | --------------------------------------------- |
| `-E`        | Run only the preprocessor (output to stdout). |
| `-D<macro>` | Define a macro for the preprocessor.          |
| `-U<macro>` | Undefine a macro.                             |

#### **Output Control**

| Flag          | Meaning                                               |
| ------------- | ----------------------------------------------------- |
| `-v`          | Verbose output (shows commands used internally).      |
| `-save-temps` | Save temporary files like preprocessed output (`.i`). |

#### **Linking Control**

| Flag             | Meaning                                                   |
| ---------------- | --------------------------------------------------------- |
| `-nostdlib`      | Don’t use the standard system startup files or libraries. |
| `-nodefaultlibs` | Don’t use default libraries (e.g., libc).                 |
| `-pthread`       | Use POSIX threads (adds `-lpthread` and relevant macros). |
---
#### Example Usage
```bash
gcc -Wall -Wextra -std=c11 -O2 -g main.c -o myprogram
```
* Enables warnings
* Uses C11 standard
* Optimizes code (`-O2`)
* Includes debug symbols
* Output is named `myprogram`
---

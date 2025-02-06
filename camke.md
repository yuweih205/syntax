| **工具链**               | **主要用途**          | **编译器**   | **链接器**    | **库**                  | **调试器**                         |
| ------------------------ | --------------------- | ------------ | ------------- | ----------------------- | ---------------------------------- |
| **GNU Toolchain（GCC）** | Linux、嵌入式         | `gcc`        | `ld (GNU ld)` | `glibc`, `musl`         | `gdb`                              |
| **LLVM/Clang**           | Linux, macOS, Android | `clang`      | `lld`         | `libc++`, `compiler-rt` | `lldb`                             |
| **MSVC（微软工具链）**   | Windows 开发          | `cl.exe`     | `link.exe`    | `msvcrt`                | `WinDbg`, `Visual Studio Debugger` |
| **MinGW-w64**            | Windows 编译 GNU 软件 | `gcc`        | `ld`          | `mingw-w64`             | `gdb`                              |
| **Intel OneAPI**         | 高性能计算（HPC）     | `icx`, `icc` | `ld`          | `Intel MKL`, `IPPS`     | `gdb`                              |
| **NVCC（NVIDIA CUDA）**  | GPU 编程              | `nvcc`       | `nvlink`      | `CUDA Runtime`          | `cuda-gdb`                         |

GNU的make工作时的执行步骤如下：

1. 读入所有的Makefile。
2. 读入被include的其它Makefile。
3. 初始化文件中的变量。
4. 推导隐式规则，并分析所有规则。
5. 为所有的目标文件创建依赖关系链。
6. 根据依赖关系，决定哪些目标要重新生成。
7. 执行生成命令。



find_package（）
link_library（）
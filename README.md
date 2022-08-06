# turq
## what's turq
   A fast runtime backend for go,c,rust,lua code. It works like a jvm,but it's always jited,so running codes in the vm is as fast as native codes.

## how it works
   Yes, codes written in go,c,rust,lua are translated to well-defined bytecodes.A dedicated interpreter is use to interpret these bytecodes execution. 
   actually, the interpreter is just a test tool for verify the correctness of the logic. A jit compiler is use to translate the bytecodes to native code at runtime, so at runtime, codes are executed as fast as the native code.
   Recently, we use the linux kernel ebpf virtual machine as the jit compiler.
## schedule
   we did migrate the vm to userspace, it can run bytecodes generated by llvm compiler. only amd64 archtecure is supported

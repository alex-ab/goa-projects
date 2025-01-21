all: build/libc_ucontext.lib.so

build/libc_ucontext.lib.so: build/getcontext.o 
	ld -o build/libc_ucontext.lib.so -soname=libc_ucontext.lib.so -shared \
	      build/getcontext.o

build/getcontext.o: x86_64/getcontext.S
	mkdir -p build
	gcc -c x86_64/getcontext.S -o build/getcontext.o

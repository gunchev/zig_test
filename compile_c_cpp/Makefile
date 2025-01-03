EXES = hello_c_zig hello_c hello_cpp hello_cpp_zig

help:
	@echo "Available targets:"
	@echo "  all: Build all executables"
	@echo "  clean: Remove all generated files"

all: $(EXES)

hello_c_zig:
	zig cc -Wall -Os -s hello.c -o hello_c_zig

hello_c:
	gcc -Wall -Os -s hello.c  -o hello_c

hello_cpp:
	g++ -Wall -Os -s -o hello_cpp hello.cpp

hello_cpp_zig:
	zig c++ -Wall -Os -s -o hello_cpp_zig hello.cpp

clean:
	rm -f $(EXES)

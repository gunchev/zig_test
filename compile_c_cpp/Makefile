all: hello_c_zig hello_c hello_cpp hello_cpp_zig

hello_c_zig:
	zig cc -Wall -Os hello.c -o hello_c_zig

hello_c:
	gcc -Wall -Os hello.c  -o hello_c

hello_cpp:
	g++ -Wall -Os -o hello_cpp hello.cpp

hello_cpp_zig:
	zig c++ -Wall -Os -o hello_cpp_zig hello.cpp

clean:
	rm -f hello_c_zig hello_c hello_cpp hello_cpp_zig

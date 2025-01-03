HELP_TARGETS = all clean
HELLO_TARGETS = hello_c hello_c_zig hello_cpp hello_cpp_zig

.PHONY: help
help:
	@echo "Available targets:"
	@echo
	@echo "    all: Compile all."
	@echo "    clean: Remove all compiled binaries."
	@echo
	@$(foreach target,$(HELLO_TARGETS), echo "    $(target): Compile only '$(target)' binary.";)

.PHONY: all
all: $(HELLO_TARGETS)
	ls -al $(HELLO_TARGETS)

hello_c:
	gcc -Wall -Os -s -o $@ hello.c

hello_c_zig:
	zig cc -Wall -Os -s -o $@ hello.c

hello_cpp:
	g++ -Wall -Os -s -o $@ hello.cpp

hello_cpp_zig:
	zig c++ -Wall -Os -s -o $@ hello.cpp

.PHONY: clean
clean:
	rm -f -- $(HELLO_TARGETS)

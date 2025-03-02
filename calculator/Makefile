CC = gcc # specify the compiler to use
CFLAGS = -Wall -Wextra -g # specify compiler flags, extra warning + debugging symbols
OBJECTS = main.o addition.o subtraction.o multiplication.o division.o # var holding list of object files

calculator: $(OBJECTS) # target is calculator, which depends on all object files as prerequisites
	$(CC) $(CFLAGS) -o calculator $(OBJECTS) # compile all object files into the executable

%.o: %.c # pattern rule: if a .o file is needed but doesn't exist, compile its corresponding .c file
	$(CC) $(CFLAGS) -c $< -o $@ # compile the .c file (first prerequisite) into the .o file (target)

clean: # phony target to remove all of the object files and the executable
	rm -f calculator $(OBJECTS) # force remove the executable (the calculator binary) and all object files

.PHONY: clean # declare clean as phony target, so make always runs it even if a file called clean exists
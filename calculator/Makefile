OBJECTS = main.o addition.o subtraction.o multiplication.o division.o # var holding list of object files

calculator: $(OBJECTS) # target is calculator, which depends on all object files as prereqs
	cc -o calculator $(OBJECTS) # compile all object files into the executable

%.o: %.c # if a .o file is needed but doesn't exist, compile its corresponding .c file
	cc -c $< -o $@ # compile the .c file (first prerequisite) into the .o file (target)

clean: # remove all of the object files and the executable
	rm -f calculator $(OBJECTS) # force remove the executable (the calculator binary) and all object files
	make calculator # recompile the calculator binary
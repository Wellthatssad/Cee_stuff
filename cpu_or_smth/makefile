CXX := gcc
CFLAGS := -g
INCLUDES := ./includes/*.h
EXECUTABLE := cpu

OBJ := *.o

build:
	make obj
	make exec
	make clean_obj
	mkdir ./build
	mv $(EXECUTABLE).exe ./build

run:
	make obj
	make exec
	./cpu.exe
	make clean_run

exec:
	$(CXX) $(OBJ) -o $(EXECUTABLE)

obj:
	$(CXX) $(INCLUDES) $(CFLAGS) -c ./src/*.c 

clean_obj:
	rm ./includes/*.gch
	rm *.o

clean_run:
	rm ./includes/*.gch
	rm *.o
	rm $(EXECUTABLE).exe

clean_build:
	rm ./build/*
	rmdir ./build
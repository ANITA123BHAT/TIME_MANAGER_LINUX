 # This makefile shall be used to create the time_manager.so shared library
#CC=g++
#OPT=-O0
#CFLAGS= -Wall -Wextra -g $(OPT)
#LIBDIR=./src

#BINARY=time
#all:$(BINARY)

#%.cpp:
#	SOURCECODE=$(foreach SRC,$(LIBDIR),$(wildcard $(SRC)/*.cpp))
#	OBJFILE=$(patsubst %.cpp,%.o,$(SOURCECODE))

#time.o:%.cpp
#	$(CC) $(CFLAGS) -c -o $@ ./src/time_manager_lib.cpp

#$(BINARY):time.o
#	$(CC) $(CFLAGS) -shared -fPIC -o libtime.so time.o 

#clean:
#	rm -rf $(BINARY) $(OBJECTS)


all:shared

#INCLUDES:-I./include

file:
#	g++ $(INCLUDES) -c ./src/time_manager_lib.cpp -o time_manager_lib.o
	g++ -c time_manager_lib.cpp -o time_manager_lib.o 

object:
	g++ -c -o time_manager_lib.o ./src/time_manager_lib.cpp

shared:object
	g++ -shared -fPIC -o libtime_lib.so time_manager_lib.o


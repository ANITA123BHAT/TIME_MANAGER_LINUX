#This makefile shall create the time-manager executable
CC=g++
INCDIRS=-I.
OPT=-O0
CFLAGS=-Wall -Wextra -g $(OPT)
LIBDIR=./src
BINARY=time

all: $(BINARY)
SOURCECODE=$(foreach SRC, $(LIBDIR), $(wildcard $(SRC)/*.cpp))
OBJEFILE=$(patsubst %.cpp, %.o ,$(SOURCECODE))
DEPENDENCIES=$(patsubst %.cpp,%.d, $(SOURCECODE))

$(BINARY):$(OBJEFILE)
	$(CC) $(CFLAGS) -o $@ $^

#%.o:%.cpp
#	$(CC) $(CFLAGS) -c -o $@ $<

clean:
	rm -rf $(BINARY) $(OBJECTS)
-include $(DEPENDENCIES)

#all:shared

#object:
#	g++ -c -o time_manager_daemon.o ./daemon/src/time_manager_deamon.cpp

#shared:object
	

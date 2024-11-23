DEBUG = 1
EXECUTABLE_NAME = main

CC = gcc
CC_STANDARD =
CC_WARNINGS = -Wall -Wextra -Wpedantic
CC_FLAGS = $(CC_WARNINGS)
LD_FLAGS = 

ifeq ($(DEBUG),1)
CC_FLAGS += -g -O0
else
CC_FLAGS += -O3
endif

COMPILER_CALL = $(CC) $(CC_FLAGS)

build: my_lib.o main.o
	$(COMPILER_CALL) my_lib.o main.o $(LD_FLAGS) -o $(EXECUTABLE_NAME)

main.o:
	$(COMPILER_CALL) main.c -c

my_lib.o:
	$(COMPILER_CALL) my_lib.c -c

execute:
	./$(EXECUTABLE_NAME)

clean:
	rm -f *.o
	rm -f main

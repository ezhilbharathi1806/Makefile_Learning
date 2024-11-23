DEBUG = 1
EXECUTABLE_NAME = main

CC = gcc
CC_STANDARD = C99
CC_WARNINGS = -Wall -Wextra -Wpedantic
CC_FLAGS = $(CC_WARNINGS)
LD_FLAGS = 

ifeq ($(DEBUG),1)
CC_FLAGS += -g -O0
else
CC_FLAGS += -O3
endif

COMPILER_CALL = $(CC) $(CC_FLAGS)

CC_OBJECTS = my_lib.o main.o

build: $(CC_OBJECTS)
	$(COMPILER_CALL) $(CC_OBJECTS) $(LD_FLAGS) -o $(EXECUTABLE_NAME)

execute:
	./$(EXECUTABLE_NAME)

clean:
	rm -f *.o
	rm -f main

##############
## PATTERNS ##
##############
# $@: the file name of the target
# $<: the name of the first ependency
# $^: the names of all prerequisites
%.o: %.c
	$(COMPILER_CALL) -c $< -o $@
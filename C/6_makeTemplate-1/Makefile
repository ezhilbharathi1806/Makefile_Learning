INCLUDE_DIR = inc
SOURCE_DIR = src
BUILD_DIR = build
EXECUTABLE_NAME = main

DEBUG = 1
ENABLE_WARNINGS = 1
WARNINGS_AS_ERRORS = 0

CC = gcc
CC_STANDARD = C99
ifeq ($(ENABLE_WARNINGS),1)
CC_WARNINGS = -Wall -Wextra -Wpedantic
else
CC_WARNINGS =
endif
ifeq ($(WARNINGS_AS_ERRORS), 1)
CC_WARNINGS += -Werror
endif
CC_FLAGS = $(CC_WARNINGS)
LD_FLAGS = 

ifeq ($(DEBUG),1)
CC_FLAGS += -g -O0
else
CC_FLAGS += -O3
endif

COMPILER_CALL = $(CC) $(CC_FLAGS) -I $(INCLUDE_DIR)

CC_SOURCES = $(wildcard $(SOURCE_DIR)/*.c)
CC_OBJECTS = $(patsubst $(SOURCE_DIR)/%.c, $(BUILD_DIR)/%.o, $(CC_SOURCES))

all: create build

create:
	@mkdir -p build

build: create $(CC_OBJECTS)
	echo $(CC_SOURCES)
	echo $(CC_OBJECTS)
	$(COMPILER_CALL) $(CC_OBJECTS) $(LD_FLAGS) -o $(BUILD_DIR)/$(EXECUTABLE_NAME)

execute:
	./$(EXECUTABLE_NAME)

clean:
	rm -f $(BUILD_DIR)/*.o
	rm -f $(BUILD_DIR)/main

##############
## PATTERNS ##
##############
# $@: the file name of the target
# $<: the name of the first ependency
# $^: the names of all prerequisites
$(BUILD_DIR)/%.o: $(SOURCE_DIR)/%.c
	$(COMPILER_CALL) -c $< -o $@


.PHONY: create build execute clean
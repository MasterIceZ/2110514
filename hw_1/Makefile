CXX=clang++
CFXXLAGS=-std=gnu++2a -Wno-macro-redefined -Wall -g
LDFLAGS=-L$(BREW_PREFIX)/lib -lglfw -framework OpenGL -framework GLUT -DGL_SILENCE_DEPRECATION

ADDFLAGS=-DOSX

BREW_PREFIX=$(shell brew --prefix)
PROJ_DIR=$(CURDIR)

TARGET=build/main

ARGS ?= $(ARGS)

INCLUDES=-I$(BREW_PREFIX)/include -I$(PROJ_DIR)/include

SRC=$(shell find src -name '*.cpp' -o -name '*.c')

all: build run

build: $(TARGET)

$(TARGET): $(SRC)
	@mkdir -p build
	$(CXX) -o $(TARGET) $(SRC) $(INCLUDES) $(LDFLAGS) $(CFXXLAGS) $(ADDFLAGS)

run:
	@./$(TARGET) $(ARGS)

clean:
	$(RM) $(TARGET)

rebuild: clean all

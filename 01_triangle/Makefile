CC = gcc

SRC = src/main.c ../third_party/glad/glad.c
OBJ = $(SRC:.c=.o)
BIN = build/base.bin

INCLUDES = -I../third_party/glad -I../third_party/glfw/include
CFLAGS = -Wall -g $(INCLUDES)
LDFLAGS = -ldl -lm -lGL -L../third_party/glfw/src -lglfw

all: build $(BIN)

build:
	mkdir -p build

$(BIN): $(OBJ)
	$(CC) $(OBJ) -o $@ $(LDFLAGS)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ) $(BIN)

.PHONY: all clean build
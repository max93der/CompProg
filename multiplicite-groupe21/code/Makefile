CC=gcc
CFLAGS=--std=c99 --pedantic -Wall -W -Wmissing-prototypes
LDFLAGS=
EXEC=multiplicite

all: $(EXEC)

multiplicite: multiplicite.o main.o
	$(CC) -o $@ $^ $(LDFLAGS)

multiplicite.o: multiplicite.c
	$(CC) -o $@ -c $< $(CFLAGS)

main.o: main.c multiplicite.h
	$(CC) -o $@ -c $< $(CFLAGS)

clean:
	rm -rf *.o

mrproper: clean
	rm -rf $(EXEC)

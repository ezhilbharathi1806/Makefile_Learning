build: my_lib.o main.o
	gcc my_lib.o main.o -o main

main.o:
	gcc main.c -c

my_lib.o:
	gcc my_lib.c -c

execute:
	./main

clean:
	rm -f *.o
	rm -f main
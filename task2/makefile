calc: main.o add.o subtract.o multiply.o
	gcc $^ -o $@

main.o: main.c
	gcc -c $<

include makefile1.mk

include makefile2.mk

include makefile3.mk

.PHONY: clean

clean:
	rm -rf *.o ./calc

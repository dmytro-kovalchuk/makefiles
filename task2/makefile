calc: main.o add.o subtract.o multiply.o
	gcc $^ -o $@

main.o: main.c
	gcc -c $<

ifeq ($(BUILD_METHOD), fflag)
.PHONY: all
all:
	make -f makefile1.mk
	make -f makefile2.mk
	make -f makefile3.mk

else ifeq ($(BUILD_METHOD), include)
include makefile1.mk
include makefile2.mk
include makefile3.mk

else
$(error ERROR! BUILD_METHOD is not set - use either fflag or include!)
endif

.PHONY: clean
clean:
	rm -rf *.o ./calc

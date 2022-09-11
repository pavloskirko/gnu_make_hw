CC = gcc
OBJ = src1.o src2.o src3.o
DEP = main.h

test: main.c $(OBJ) $(DEP)
	$(CC) $^ -o $@ 

ifndef MAKE_INCLUDE

src1.o: src1.c
	make -f make1.mk

src2.o: src2.c
	make -f make2.mk

src3.o: src3.c
	make -f make3.mk

endif # MAKE_INCLUDE

ifdef MAKE_INCLUDE

include make1.mk

include make2.mk

include make3.mk

endif

.PHONY: clean

clean: 
	rm -rf *.o test *.gch
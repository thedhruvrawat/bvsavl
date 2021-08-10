CC=gcc
CFLAGS=-g3

all: testAVLTree
	time ./testAVLTree

test: all
	valgrind -q --leak-check=yes ./testAVLTree

testAVLTree: testAVLTree.o avlTree.o
	$(CC) $(CFLAGS) -o $@ $^

testAVLTree.o avlTree.o: avlTree.h

clean:
	$(RM) testAVLTree *.o

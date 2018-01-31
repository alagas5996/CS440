#My standard macros
EXEC = -g -std=c++11 -pthread -O2 -Wall -Wextra -Wundef -pedantic
FILE = -g -std=c++11 -pthread -O2 -Wall -Wextra -Wundef -pedantic -c

#Compile
all: testCompile

testCompile: test.o
	g++ $(EXEC) Deque.o test.o -o test

test.o: test.cpp Deque.o
	g++ $(FILE) test.cpp -o test.o

Deque.o: Deque.hpp
	g++ $(FILE) Deque.hpp -o Deque.o

#Test
test: all
	./test

#Cleanup
clean:
	rm -rf *.o test

cleaner: clean
	reset

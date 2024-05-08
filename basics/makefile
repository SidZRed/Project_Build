main.out: main.o sub1.o sub2.o
	g++ main.o sub1.o sub2.o -o main.out

sub1.o: sub1.cpp
	g++ -c sub1.cpp -o sub1.o

sub2.o: sub2.cpp
	g++ -c sub2.cpp -o sub2.o

main.o: main.cpp
	g++ -c main.cpp -o main.o


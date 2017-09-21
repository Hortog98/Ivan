all: program

program:	mkDir project.o functions.o
		g++ build/project.o build/functions.o -o bin/project.exe

project.o:	project.cpp
		g++ -I library -Wall -Werror -c project.cpp -o build/project.o

functions.o:	functions.cpp
		g++ -I library -Wall -Werror -c functions.cpp -o build/functions.o

test:		mkDir modul_test.o result_test.o 
		gcc build/modul_test.o build/result_test.o -o bin/test.exe

modul_test.o:		tests/modul_test.c
		gcc -I library -I main -c tests/modul_test.c -o build/modul_test.o

result_test.o:	tests/result_test.c
		gcc -I library -I main -c tests/result_test.c -o build/result_test.o

mkDir:	bin build

bin:
	test ! -d bin && mkdir bin

build:
	test ! -d build && mkdir build

clean:
	rm -r bin
	rm -r build

run:
	./bin/project.exe
runtest:
	./bin/test.exe

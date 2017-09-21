all: prog test

test:			mkDir modul_test.o result_test.o

				gcc build/modul_test.o build/result.o  -o bin/tests

modul_test.o:	tests/modul_test.c
		
				gcc -I tests/modul_test.c -o build/modul_test.o


result_test.o:	tests/result_test.c

				gcc -I tests/result_test.c -o build/result_test.o


mkDir:			bin build


bin:			
				test ! -d bin && mkdir bin


build:
				test ! -d build && mkdir build


.PHONY:			clean


clean:
				rm -r bin
				rm -r build


run:
				./bin/prog


runtest:
				./bin/tests

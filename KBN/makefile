all: prog test

prog:			mkDir main.o functions.o

				g++ build/main.o build/functions.o -o bin/IrregularVerbs


main.o:			src/main.cpp

				g++ -I thirdparty -Wall -Werror -c src/main.cpp -o build/main.o


functions.o:	src/functions.cpp

				g++ -I thirdparty -Wall -Werror -c src/functions.cpp -o build/functions.o	


test:			mkDir main_test.o ran_test.o grac_test.o perc_test.o

				gcc build/ran_test.o build/main.o build/grac_test.o build/perc_test.o -o bin/Tests


main_test.o:	tests/main.c
		
				gcc -I thirdparty -I src -c tests/main.c -o build/main.o


ran_test.o:		tests/ran_test.c
		
				gcc -I thirdparty -I src -c tests/ran_test.c -o build/ran_test.o


grac_test.o:	tests/grac_test.c
		
				gcc -I thirdparty -I src -c tests/grac_test.c -o build/grac_test.o


perc_test.o:	tests/perc_test.c
		
				gcc -I thirdparty -I src -c tests/perc_test.c -o build/perc_test.o	


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

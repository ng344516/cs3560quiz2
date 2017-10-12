#CS3560 Makefile - quiz 2
#Nic Gill ng344516
all: build doczip

clean:
	rm -rf *.o core *.core

build: course.o college.o collegemain.o
	g++ -o myexe course.o college.o collegemain.o
course.o: course.h course.cc
	g++ -c course.cc
college.o: college.h college.cc
	g++ -c college.cc
collegemain.o: collegemain.cc
	g++ -c collegemain.cc

myexe: course.o college.o collegemain.o
	g++ -o myexe course.o college.o collegemain.o
course.o: course.h course.cc
	g++ -c course.cc
college.o: college.h college.cc
	g++ -c college.cc
collegemain.o: collegemain.cc
	g++ -c collegemain.cc

doc:
	doxygen config

doczip: doc
	tar cvzf ng344516_quiz2.tar.gz college.cc college.h collegemain.cc course.cc course.h node.h tarray.h makefile html

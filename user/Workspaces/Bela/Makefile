# Makefile for Bela / Beaglebone Black. Produces shared library dspfilters.so.

OBJECTS = Bessel.o Biquad.o Butterworth.o Cascade.o ChebyshevI.o ChebyshevII.o Custom.o Design.o Documentation.o Elliptic.o Filter.o Legendre.o Param.o PoleFilter.o RBJ.o RootFinder.o State.o

%.o : ../../../shared/DSPFilters/source/%.cpp
	gcc -fPIC -I ../../../shared/DSPFilters/include -c $< -o $@

DSPFilters.so : ${OBJECTS}
	gcc ${OBJECTS} --shared -o $@

clean:
	- rm *.o
	- rm *.so


SOURCES=$(addsuffix .cpp, Snipes $(addprefix sdl/, console keyboard sound timer))
CFLAGS=-Werror -Wall -Wextra -std=c++11 $(shell sdl2-config --cflags)
CFLAGS2=-O3
#CFLAGS2=-Og -g -fsanitize=address -fsanitize=undefined
LDFLAGS=$(shell sdl2-config --libs) -lm -lSDL2_ttf
CXX=g++
#CXX="clang++"

snipes : $(SOURCES) config.h GNUmakefile
	$(CXX) -o $@ $(CFLAGS) $(CFLAGS2) $(SOURCES) $(LDFLAGS)

clean :
	rm -f snipes

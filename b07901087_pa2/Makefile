CC=g++
LDFLAGS=-std=c++11 -O3 -lm
SOURCES=src/module.cpp src/floorplanner.cpp src/main.cpp
OBJECTS=$(SOURCES:.c=.o)
EXECUTABLE=fp
INCLUDES=src/module.h src/floorplanner.h 

all: $(SOURCES) bin/$(EXECUTABLE)

bin/$(EXECUTABLE): $(OBJECTS)
	$(CC) $(LDFLAGS) $(OBJECTS) -o $@

%.o:  %.c  ${INCLUDES}
	$(CC) $(CFLAGS) $< -o $@
plt:
	$(CC) $(LDFLAGS) src/plot.cpp -o $@
clean:
	rm -rf *.o bin/$(EXECUTABLE)
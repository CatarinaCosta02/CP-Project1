CC = gcc
SRC = src/
CFLAGS = -pg -fopenmp -O2

.DEFAULT_GOAL = MD.exe

MD.exe: $(SRC)/MD.cpp
	$(CC) $(CFLAGS) $(SRC)MD.cpp -lm -o MD.exe

clean:
	rm ./MD.exe

run:
	sudo perf stat -e instructions,cycles,cache-misses ./MD.exe < inputdata.txt
prof:
	gprof MD.exe gmon.out | gprof2dot -w | dot -Tpng -o output.png
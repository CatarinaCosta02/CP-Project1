CC = gcc
SRC = src/
CFLAGS = -O2

.DEFAULT_GOAL = MD.exe

MD.exe: $(SRC)/MD.cpp
	$(CC) $(CFLAGS) $(SRC)MD.cpp -lm -o MD.exe

clean:
	rm ./MD.exe

run:
	sudo perf stat -e instructions,cycles ./MD.exe < inputdata.txt
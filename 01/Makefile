all: cpu mem threads io

clean:
	rm -f cpu mem threads io

cpu: cpu.c common.h
	gcc -o cpu cpu.c -Wall

mem: mem.c common.h
	gcc  -Wall -no-pie -o mem mem.c
	# setarch $(uname -m) -R ./mem 1

threads: threads.c common.h common_threads.h
	gcc -o threads threads.c -Wall -pthread

io: io.c common.h
	gcc -o io io.c -Wall


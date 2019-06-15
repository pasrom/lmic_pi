CC=${CROSS_COMPILE}gcc
CFLAGS+=-I../../lmic -I/usr/local/include -Winline -pipe -g3
LDFLAGS+=-L/usr/local/lib -lwiringPi -lpthread -lm -lcrypt -lrt

thethingsnetwork-send-v1: thethingsnetwork-send-v1.cpp
	cd ../../lmic && $(MAKE)
	$(CC) $(CFLAGS) -o thethingsnetwork-send-v1 thethingsnetwork-send-v1.cpp ../../lmic/*.o $(LDFLAGS)

all: thethingsnetwork-send-v1

.PHONY: clean

clean:
	rm -f *.o thethingsnetwork-send-v1
	rm -f ../../lmic/*.o

# This is the Makefile for the imc2 utils

DEFINES=
ICE_OBJ=iced.o ice.o
ICE_DEF=-DICED
#DEFINES=-DNO_VSNPRINTF=1
CFLAGS=-Wall -g3 $(DEFINES) $(ICE_DEF)
LFLAGS=
#LFLAGS=-lnsl -lsocket

all: router webserver webclient

router: router.o imc.o imc-interp.o imc-version.o imc-mail.o imc-util.o imc-events.o imc-config.o $(ICE_OBJ)
	rm -f router
	$(CC) $(CFLAGS) $(LFLAGS) -o router router.o imc.o imc-interp.o imc-version.o imc-mail.o imc-util.o imc-events.o imc-config.o $(ICE_OBJ)


webserver: webserver.o imc.o imc-interp.o imc-version.o imc-mail.o imc-util.o imc-events.o imc-config.o
	rm -f webserver
	$(CC) $(CFLAGS) $(LFLAGS) -o webserver webserver.o imc.o imc-interp.o imc-version.o imc-mail.o imc-util.o imc-events.o imc-config.o

webclient: webclient.o
	rm -f webclient
	$(CC) $(CFLAGS) $(LFLAGS) -o webclient webclient.o


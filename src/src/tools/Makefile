# Generated automatically from Makefile.in by configure.
#
# Makefile.in for UAE tools
#


CC        = gcc
LDFLAGS   = 
CFLAGS    = -g -O2 -D__inline__=inline -DUAE_CONSOLE
LIBRARIES = 

INSTALL         = @INSTALL@
INSTALL_PROGRAM = @INSTALL_PROGRAM@
INSTALL_DATA    = @INSTALL_DATA@
prefix          = /usr/local
exec_prefix     = ${prefix}
bindir          = ${exec_prefix}/bin
libdir          = ${exec_prefix}/lib
sysconfdir      = ${prefix}/etc

VPATH = /data/uae-0.8.29/src/tools

.SUFFIXES: .o .c .h .m .i .S

INCLUDES=-I. -I/data/uae-0.8.29/src/tools/../include/ -I/data/uae-0.8.29/src/tools

all: gencpu build68k genblitter cpuopti

install:


clean:
	-rm -f *.o cpudefs.c lientoscr.c
	-rm -f gencpu genblitter cpuopti build68k


streifenfrei: clean
	rm -f Makefile config.* sysconfig.h

genblitter: genblitter.o blitops.o writelog.o
	$(CC) $(LDFLAGS) -o genblitter genblitter.o blitops.o writelog.o
build68k: build68k.o writelog.o
	$(CC) $(LDFLAGS) -o build68k build68k.o writelog.o
cpuopti: cpuopti.o writelog.o
	$(CC) $(LDFLAGS) -o cpuopti cpuopti.o writelog.o
gencpu: gencpu.o readcpu.o cpudefs.o missing.o writelog.o
	$(CC) $(LDFLAGS) -o gencpu gencpu.o readcpu.o cpudefs.o missing.o writelog.o

custom.o: blit.h
drawing.o: linetoscr.c

cpudefs.c: build68k /data/uae-0.8.29/src/tools/../table68k
	./build68k </data/uae-0.8.29/src/tools/../table68k >cpudefs.c

# Normally I'd move the programs into this directory, but given that CVS
# sucks I have no choice but to leave them in their previous directory.
missing.o: /data/uae-0.8.29/src/tools/../missing.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../missing.c -o $@
readcpu.o: /data/uae-0.8.29/src/tools/../readcpu.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../readcpu.c -o $@
writelog.o: /data/uae-0.8.29/src/tools/../writelog.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../writelog.c -o $@
genblitter.o: /data/uae-0.8.29/src/tools/../genblitter.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../genblitter.c -o $@
gencpu.o: /data/uae-0.8.29/src/tools/../gencpu.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../gencpu.c -o $@
build68k.o: /data/uae-0.8.29/src/tools/../build68k.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../build68k.c -o $@
blitops.o: /data/uae-0.8.29/src/tools/../blitops.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../blitops.c -o $@
cpuopti.o: /data/uae-0.8.29/src/tools/../cpuopti.c
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(DEBUGFLAGS) /data/uae-0.8.29/src/tools/../cpuopti.c -o $@

.c.o:
	$(CC) $(INCLUDES) -c $(INCDIRS) $(CFLAGS) $(X_CFLAGS) $(DEBUGFLAGS) $(CFLAGS_$@) $< -o $@
.c.s:
	$(CC) $(INCLUDES) -S $(INCDIRS) $(CFLAGS) $(X_CFLAGS) $(DEBUGFLAGS) $< -o $@
.c.i:
	$(CC) $(INCLUDES) -E $(INCDIRS) $(CFLAGS) $(X_CFLAGS) $(DEBUGFLAGS) $< > $@


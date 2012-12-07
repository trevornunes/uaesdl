#
# Top-level Makefile for UAE
#

SHELL=/bin/bash
INSTALL=/usr/bin/install -c
INSTALL_PROGRAM=${INSTALL}

prefix          = /usr/local
datarootdir     = ${prefix}/share
datadir         = ${datarootdir}
exec_prefix     = ${prefix}
bindir          = ${exec_prefix}/bin
libdir          = ${exec_prefix}/lib
sysconfdir      = ${prefix}/etc
top_srcdir	= .

mkinstalldirs=$(SHELL) $(top_srcdir)/mkinstalldirs

CONFIGS = a500 a500-expanded a500plus a1200 a4000 poweruser

all:
	cd src && $(MAKE)
	cp src/uae .
	cp src/readdisk .

install:
	$(mkinstalldirs) $(DESTDIR)$(bindir)
	$(mkinstalldirs) $(DESTDIR)$(datadir)/uae/roms
	$(mkinstalldirs) $(DESTDIR)$(datadir)/uae/configs
	for x in $(CONFIGS); do \
		$(INSTALL) $(top_srcdir)/configs/$$x.uae $(DESTDIR)$(datadir)/uae/configs; \
	done
	$(INSTALL_PROGRAM) uae $(DESTDIR)$(bindir)

clean:
	cd src && $(MAKE) clean
	rm -f uae readdisk 

streifenfrei:
	cd src && $(MAKE) streifenfrei
	rm -f uae readdisk
	rm -f config.cache config.log config.status Makefile
	rm -f confdefs.h

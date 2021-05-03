#***********************************************************************
CROSS_COMPILE=
CC=$(CROSS_COMPILE)cc
COPTS=-O2 -g -pipe

DESTDIR = $(INSTROOT)//usr/local
LIBDIR = $(DESTDIR)/lib/pppd/$(VERSION)

VERSION = $(shell awk -F '"' '/VERSION/ { print $$2; }' ../../patchlevel.h)

CFLAGS	= $(COPTS) -I. -I../.. -I../../../include -fPIC
LDFLAGS_SHARED	= -shared
INSTALL	= install

PLUGINS := pppol2tp.so openl2tp.so

all: $(PLUGINS)

%.so: %.o
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $(LDFLAGS_SHARED) $^ $(LIBS)

install: all
	$(INSTALL) -d -m 755 $(LIBDIR)
	$(INSTALL) -c -m 755 $(PLUGINS) $(LIBDIR)

clean:
	rm -f *.o *.so

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<

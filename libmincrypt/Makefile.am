AM_CFLAGS := -Wundef \
        -Wstrict-prototypes \
        -Wno-trigraphs \
        -g -O0 \
        -fno-inline \
        -fno-short-enums \
        -fpic

AM_CPPFLAGS := \
              -I. \
              -I../include

AM_LDFLAGS := -shared -version-info 1:0:0
c_sources := rsa.c sha.c sha256.c

library_includedir := $(includedir)/mincrypt
library_include_HEADERS := $(abs_top_srcdir)/include/mincrypt/rsa.h \
	$(abs_top_srcdir)/include/mincrypt/sha.h \
	$(abs_top_srcdir)/include/mincrypt/sha256.h \
	$(abs_top_srcdir)/include/mincrypt/hash-internal.h

lib_LTLIBRARIES := libmincrypt.la
libmincrypt_la_SOURCES := $(c_sources) $(h_sources)
libmincrypt_la_CFLAGS := $(AM_CFLAGS) -DUSE_GLIB
libmincrypt_la_CPPFLAGS := $(AM_CPPFLAGS) -DUSE_GLIB
libmincrypt_la_LIBADD := -lm -lpthread
libmincrypt_la_LDFLAGS := -all-static

pkgconfigdir := $(libdir)/pkgconfig
pkgconfig_DATA := libmincrypt.pc
EXTRA_DIST := $(pkgconfig_DATA)

bin_PROGRAMS = mkbootimg

mkbootimg_SOURCES := \
	mkbootimg.c \
	mkbootimg.h

mkbootimg_CFLAGS = -O2 \
	-g \
	-Wall \
	-Wno-unused-parameter \
	-I../include

mkbootimg_LDFLAGS = -all-static

mkbootimg_LDADD = ../libmincrypt/libmincrypt.la


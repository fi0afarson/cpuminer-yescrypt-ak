
if WANT_JANSSON
JANSSON_INCLUDES= -I$(top_srcdir)/compat/jansson
else
JANSSON_INCLUDES=
endif

EXTRA_DIST	= example-cfg.json nomacro.pl

SUBDIRS		= compat

INCLUDES	= $(PTHREAD_FLAGS) -fno-strict-aliasing $(JANSSON_INCLUDES)

bin_PROGRAMS	= minerd-ak

dist_man_MANS	= minerd-ak.1

minerd_ak_SOURCES	= elist.h miner.h compat.h \
		  cpu-miner.c util.c \
		  sha256.c sha256_shani.c yespower.c yespower.h yespower-opt.c
minerd_ak_LDFLAGS	= $(PTHREAD_FLAGS)
minerd_ak_LDADD	= @LIBCURL@ @JANSSON_LIBS@ @PTHREAD_LIBS@ @WS2_LIBS@
minerd_ak_CPPFLAGS = @LIBCURL_CPPFLAGS@


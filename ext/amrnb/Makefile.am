plugin_LTLIBRARIES = libgstamrnb.la

libgstamrnb_la_SOURCES = \
	amrnb.c \
	amrnbdec.c \
	amrnbenc.c

libgstamrnb_la_CFLAGS = -DGST_USE_UNSTABLE_API $(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_BASE_CFLAGS) $(GST_CFLAGS) $(AMRNB_CFLAGS)
libgstamrnb_la_LIBADD = $(GST_PLUGINS_BASE_LIBS) \
        -lgstaudio-@GST_MAJORMINOR@ \
        $(GST_BASE_LIBS) $(GST_LIBS) $(AMRNB_LIBS)
libgstamrnb_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS)
if !GST_PLUGIN_BUILD_STATIC
libgstamrnb_la_LIBTOOLFLAGS = --tag=disable-static
endif

noinst_HEADERS = \
	amrnbdec.h \
	amrnbenc.h

presetdir = $(datadir)/gstreamer-$(GST_MAJORMINOR)/presets
preset_DATA = GstAmrnbEnc.prs

EXTRA_DIST = $(preset_DATA)

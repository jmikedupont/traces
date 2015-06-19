AM_CPPFLAGS = -I ../include  $(CLANG_CFLAGS) -std=c++11

noinst_LTLIBRARIES = libtrace_instrumentor_priv.la
lib_LTLIBRARIES = libtrace_instrumentor_pub.la
libtrace_instrumentor_priv_la_SOURCES=TraceCall.h trace_instrumentor.cpp
libtrace_instrumentor_priv_la_LDFLAGS = -all-static -L../libtrace   $(CLANG_LDFLAGS) -Wl,-Bstatic
libtrace_instrumentor_priv_la_LIBADD  = -ltrace  $(CLANG_LIBS)


libtrace_instrumentor_pub_la_SOURCES=trace_instrumentor_pub.cpp
libtrace_instrumentor_pub_la_LDFLAGS = -L../libtrace -static
libtrace_instrumentor_pub_la_LIBADD  =   -ltrace_instrumentor_priv 


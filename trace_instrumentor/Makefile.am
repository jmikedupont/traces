AM_CPPFLAGS = -I ../include -I /usr/lib/llvm-3.5/include/ -std=c++11

lib_LTLIBRARIES = libtrace_instrumentor.la
libtrace_instrumentor_la_SOURCES=TraceCall.h trace_instrumentor.cpp
libtrace_instrumentor_la_LDFLAGS = -L../ -L/usr/lib/llvm-3.5/lib/
libtrace_instrumentor_la_LIBADD  = -ltrace -lclang

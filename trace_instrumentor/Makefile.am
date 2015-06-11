AM_CPPFLAGS = -I ../include  $(CLANG_CFLAGS) -std=c++11

lib_LTLIBRARIES = libtrace_instrumentor.la
libtrace_instrumentor_la_SOURCES=TraceCall.h trace_instrumentor.cpp
libtrace_instrumentor_la_LDFLAGS = -L../  $(CLANG_LDFLAGS)
libtrace_instrumentor_la_LIBADD  = -ltrace $(CLANG_LIBS) /usr/lib/llvm-3.7/lib/libclangSerialization.a

AM_CPPFLAGS = -I ../include -I /usr/lib/llvm-3.7/include/ -DNDEBUG -D_GNU_SOURCE -D__STDC_CONSTANT_MACROS -D__STDC_FORMAT_MACROS -D__STDC_LIMIT_MACROS -g -O2 -fomit-frame-pointer -std=c++11 -fvisibility-inlines-hidden -fno-exceptions -fPIC -Woverloaded-virtual -ffunction-sections -fdata-sections -Wcast-qual

lib_LTLIBRARIES = libtrace_instrumentor.la
libtrace_instrumentor_la_SOURCES=TraceCall.h trace_instrumentor.cpp
libtrace_instrumentor_la_LDFLAGS = -L../ -L/usr/lib/llvm-3.7/lib/
libtrace_instrumentor_la_LIBADD  = -ltrace -lclang

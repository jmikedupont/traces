AC_INIT([traces], [1.0])
AM_INIT_AUTOMAKE()

AC_CONFIG_HEADERS([config.h:config.hin])     
AC_PROG_CC
AC_PROG_CXX
LT_INIT
AC_PROG_LIBTOOL
AC_ARG_WITH([llvm-prefix],
    [AS_HELP_STRING([--with-llvm-prefix],
        [Prefix for LLVM installations in non-standard locations])],
    [llvm_prefix="$withval"],
    [llvm_prefix=""])

AC_ARG_WITH([llvm-version],
    [AS_HELP_STRING([--with-llvm-version],
        [Version for LLVM version, eg 3.7])],
    [llvm_version="-$withval"],
    [llvm_version=""])

AC_PATH_PROG([LLVM_CONFIG], [llvm-config${llvm_version}], [no], ["$llvm_prefix/bin"])
if test -x $LLVM_CONFIG; then
    CLANG_CFLAGS=`$LLVM_CONFIG --cflags`
    AC_SUBST([CLANG_CFLAGS])

    CLANG_LDFLAGS="`$LLVM_CONFIG --ldflags` -lclang"
    AC_SUBST([CLANG_LDFLAGS])

    CLANG_LIBS="`$LLVM_CONFIG --libs`"
    AC_SUBST([CLANG_LIBS])
    
else
    AC_MSG_ERROR([Can not find llvm-config. Please, specify the llvm-prefix])
fi

AC_CONFIG_FILES([Makefile
trace_dumper/Makefile
trace_reader/Makefile
libtrace/Makefile
interactive_reader/Makefile
trace_instrumentor/Makefile
])
AC_OUTPUT


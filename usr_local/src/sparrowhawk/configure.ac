AC_INIT([Sparrowhawk], [0.1.0], [rws@google.com])
AM_INIT_AUTOMAKE([foreign nostdinc -Wall -Werror])

AM_PROG_AR

CXXFLAGS="$CXXFLAGS -std=c++11"

AC_PROG_CXX
AC_DISABLE_STATIC
AC_PROG_LIBTOOL

AC_CONFIG_SRCDIR([src/lib/normalizer.cc])
AC_CONFIG_FILES([
  Makefile
  src/Makefile
  src/include/Makefile
  src/lib/Makefile
  src/proto/Makefile
])

AC_CONFIG_MACRO_DIR([m4])
AC_LANG([C++])

AC_CHECK_HEADER([fst/fst.h], [],
 [AC_MSG_ERROR([fst/fst.h header not found])]
)

AC_CHECK_HEADER([fst/extensions/far/far.h], [],
 [AC_MSG_ERROR([fst/extensions/far/far.h header not found])]
)

AC_CHECK_HEADER([fst/extensions/pdt/pdt.h], [],
 [AC_MSG_ERROR([fst/extensions/pdt/pdt.h header not found])]
)

dnl TODO(rws): add mpdt at some point
dnl AC_CHECK_HEADER([fst/extensions/mpdt/mpdt.h], [],
dnl  [AC_MSG_ERROR([fst/extensions/mpdt/mpdt.h header not found])]
dnl )

AC_CHECK_HEADER([thrax/thrax.h], [],
 [AC_MSG_ERROR([thrax/thrax.h header not found])]
)

AC_CHECK_HEADER([re2/re2.h], [],
 [AC_MSG_ERROR([re2/re2.h header not found])]
)

AC_CHECK_HEADER([google/protobuf/message.h], [],
 [AC_MSG_ERROR([google/protobuf/message.h header not found])]
)

AC_CHECK_PROG([PROTOC], [protoc], [protoc])
AS_IF([test "x${PROTOC}" == "x"],
    [AC_MSG_ERROR([ProtoBuf compiler "protoc" not found.])])

AC_OUTPUT

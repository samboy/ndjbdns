#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.63])
AC_INIT([ndjbdns], [1.06], [pj.pandit@yahoo.co.in])
#AM_INIT_AUTOMAKE
#AM_MAINTAINER_MODE
AC_CONFIG_SRCDIR([dnsip.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CXX
AC_PROG_AWK
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_RANLIB
#PKG_CHECK_EXISTS([systemd], [have_systemd=yes], [have_systemd=no])
#AM_CONDITIONAL([HAVE_SYSTEMD], [test x$have_systemd = xyes])

# Checks for libraries.

# Checks for header files.
AC_HEADER_MAJOR
AC_CHECK_HEADERS([fcntl.h netinet/in.h stdlib.h string.h sys/param.h sys/socket.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_UID_T
AC_TYPE_OFF_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_TYPE_UINT32_T

# Checks for library functions.
AC_FUNC_CHOWN
AC_FUNC_FORK
AC_FUNC_MALLOC
AC_FUNC_MMAP
AC_CHECK_FUNCS([dup2 fchdir gethostname gettimeofday memset mkdir munmap select setenv socket strdup strndup strrchr])

AC_CONFIG_FILES([Makefile
                 etc/Makefile
                 etc/ip/Makefile
                 etc/init.d/Makefile
                 etc/servers/Makefile
                 etc/systemd/Makefile])
AC_OUTPUT

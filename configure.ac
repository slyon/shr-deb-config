AC_PREREQ([2.65])
AC_INIT([shr-config], [0.1], [http://www.shr-project.org])
AC_CONFIG_SRCDIR([Makefile.am])
AC_SUBST(DATADIR, $datadir)
AC_SUBST(BINDIR, $bindir)

AM_INIT_AUTOMAKE

################################################################################
# Binaries
################################################################################
AC_CHECK_PROG([EET], [eet], [true], [false])
if test "x$EET" = "xtrue"; then
	AC_PATH_PROG([EET], [eet], [not found])
else
	AC_MSG_ERROR([*** eet not found])
fi

AC_CHECK_PROG([EDJECC], [edje_cc], [true], [false])
if test "x$EDJECC" = "xtrue"; then
	AC_PATH_PROG([EDJECC], [edje_cc], [not found])
else
	AC_MSG_ERROR([*** edje_cc not found])
fi

################################################################################
# Output
################################################################################
AC_CONFIG_FILES([
Makefile
conf/Makefile
conf/gta04/Makefile
conf/gta04/e/Makefile
conf/gta04/e/illume/Makefile
conf/gta04/fso/Makefile
conf/gta04/misc/Makefile
conf/gta04/udev/Makefile
conf/gta04/x11/Makefile
conf/generic/Makefile
conf/generic/e/Makefile
conf/generic/fso/Makefile
conf/generic/misc/Makefile
])
AC_OUTPUT

################################################################################
# Info
################################################################################
echo
echo "------------------------------------------------------------------------"
echo "$PACKAGE_NAME $PACKAGE_VERSION"
echo "------------------------------------------------------------------------"
echo "Configuration Options:"
echo
echo "  edje_cc .............................: $EDJECC"
echo "  eet .................................: $EET"
echo
echo "------------------------------------------------------------------------"
echo
echo "Now type 'make' to compile and 'make install' to install this package."

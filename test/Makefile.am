#######################################
# The list of executables we are building seperated by spaces
# the 'bin_' indicates that these build products will be installed
# in the $(bindir) directory. For example /usr/bin
#bin_PROGRAMS=test

# Because a.out is only a sample program we don't want it to be installed.
# The 'noinst_' prefix indicates that the following targets are not to be
# installed.
noinst_PROGRAMS=test

#######################################
# Build information for each executable. The variable name is derived
# by use the name of the executable with each non alpha-numeric character is
# replaced by '_'. So a.out becomes a_out and the appropriate suffex added.
# '_SOURCES' for example.

ACLOCAL_AMFLAGS=-I ../m4

# Sources for the a.out 
test_SOURCES= test.cpp

# Libraries for a.out
test_LDADD = $(top_srcdir)/libegihash/libegihash.la

# Linker options for a.out
test_LDFLAGS = -rpath `cd $(top_srcdir);pwd`/libegihash/.libs $(BOOST_UNIT_TEST_FRAMEWORK_LIB)

# Compiler options for a.out
test_CPPFLAGS = -I$(top_srcdir)/include -DBOOST_TEST_DYN_LINK -DBOOST_TEST_MAIN

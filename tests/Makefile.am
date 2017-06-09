noinst_PROGRAMS = $(TEST_PROGS)

PRODUCTION_CODE_INCLUDES = -I$(top_srcdir)/src
PRODUCTION_CODE_LIBS = $(top_builddir)/src/lib%autotools_project_template%.la

AM_CPPFLAGS = \
	$(CPPUTEST_CFLAGS)\
	$(PRODUCTION_CODE_INCLUDES)

AM_CFLAGS =	-Werror\
	-Wall\
	-g

AM_CXXFLAGS = $(AM_CFLAGS)
#AM_CXXFLAGS += -std=c++11

TEST_PROGS = %autotools_project_template%_tests

%autotools_project_template%_tests_SOURCES = %autotools_project_template%_tests.cpp
%autotools_project_template%_tests_LDADD = $(CPPUTEST_LIBS)\
	$(PRODUCTION_CODE_LIBS)

check_PROGRAMS = $(TEST_PROGS)

TESTS = $(TEST_PROGS)

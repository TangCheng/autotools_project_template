AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
	$(DEPENDENCIES_CFLAGS)

AM_CFLAGS =\
	-Wextra
	-Werror\
	-Wall\
	-g

AM_CXXFLAGS = $(AM_CFLAGS)
#AM_CXXFLAGS += -std=c++11

if ENABLE_TESTS
lib%autotools_project_template%_la_includedir = $(includedir)/%autotools_project_template%

lib_LTLIBRARIES = lib%autotools_project_template%.la

lib%autotools_project_template%_la_SOURCES = \
	%autotools_project_template%.c

#lib%autotools_project_template%_la_CPPFLAGS = $(BOOST_CPPFLAGS)

lib%autotools_project_template%_la_LDFLAGS = 
#lib%autotools_project_template%_la_LDFLAGS += $(BOOST_*_LDFLAGS)

lib%autotools_project_template%_la_LIBADD = $(DEPENDENCIES_LIBS)
#lib%autotools_project_template%_la_LIBADD += $(BOOST_*_LIBS)

lib%autotools_project_template%_la_include_HEADERS = \
	%autotools_project_template%.h

#pkgconfigdir = $(libdir)/pkgconfig
#pkgconfig_DATA = %autotools_project_template%.pc

#EXTRA_DIST = \
#	%autotools_project_template%.pc.in
endif

bin_PROGRAMS = %autotools_project_template%

%autotools_project_template%_SOURCES = \
	%autotools_project_template%.c

%autotools_project_template%_CFLAGS = $(AM_CFLAGS)
#%autotools_project_template%_CPPFLAGS = $(BOOST_CPPFLAGS)
%autotools_project_template%_CXXFLAGS = $(AM_CXXFLAGS)

%autotools_project_template%_LDFLAGS = $(AM_LDFLAGS)
#%autotools_project_template%_LDFLAGS += $(BOOST_*_LDFLAGS)

%autotools_project_template%_LDADD = $(DEPENDENCIES_LIBS)
#%autotools_project_template%_LDADD += $(BOOST_*_LIBS)

if ENABLE_TESTS
if ENABLE_COVERAGE
AM_CFLAGS +=\
	-fprofile-arcs\
	-ftest-coverage

lib%autotools_project_template%_la_LIBADD += -lgcov
endif
endif

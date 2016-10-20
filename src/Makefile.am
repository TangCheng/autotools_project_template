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

lib%autotools_project_template%_la_includedir = $(includedir)/%autotools_project_template%

lib_LTLIBRARIES = lib%autotools_project_template%.la

lib%autotools_project_template%_la_SOURCES = \
	%autotools_project_template%.c

lib%autotools_project_template%_la_LDFLAGS = 
 
lib%autotools_project_template%_la_LIBADD= $(DEPENDENCIES_LIBS)

lib%autotools_project_template%_la_include_HEADERS = \
	%autotools_project_template%.h

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = %autotools_project_template%.pc

EXTRA_DIST = \
	%autotools_project_template%.pc.in

if ENABLE_TESTS
AM_CFLAGS +=\
	-fprofile-arcs\
	-ftest-coverage

if ENABLE_COVERAGE
lib%autotools_project_template%_la_LIBADD += -lgcov
endif
endif

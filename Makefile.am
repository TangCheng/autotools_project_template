ACLOCAL_AMFLAGS = -I m4

SUBDIRS = src

if ENABLE_TESTS
SUBDIRS += tests
endif

DIST_SUBDIRS = $(SUBDIRS)

%autotools_project_template%docdir = ${prefix}/doc/%autotools_project_template%
%autotools_project_template%doc_DATA = \
	README\
	COPYING\
	AUTHORS\
	ChangeLog\
	INSTALL\
	NEWS


EXTRA_DIST = $(%autotools_project_template%doc_DATA)


# Remove doc directory on uninstall
uninstall-local:
	-rm -r $(%autotools_project_template%docdir)

coverage:
if ENABLE_COVERAGE
	gcovr -x -r .. -e ".+\.test\.cpp" --object-directory=src > coverage.xml
else
	@echo "To generate coverage report, please run ./configure with --enable-coverage"
endif

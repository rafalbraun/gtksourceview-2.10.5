INCLUDES = 				\
	-DDATADIR=\""$(datadir)"\" 	\
	-DG_LOG_DOMAIN=\"GtkSourceView\"\
	-I$(top_srcdir) -I$(srcdir) 	\
	-DTOP_SRCDIR=\""$(ABS_TOP_SRCDIR)"\"\
	$(DISABLE_DEPRECATED)		\
	$(WARN_CFLAGS) 			\
	$(DEP_CFLAGS)			\
	$(TESTS_CFLAGS)

noinst_PROGRAMS = $(TEST_PROGS) $(UNIT_TEST_PROGS)
TESTS = $(UNIT_TEST_PROGS)

TEST_PROGS = test-widget
test_widget_SOURCES = test-widget.c
test_widget_LDADD = 			\
	$(top_builddir)/gtksourceview/libgtksourceview-2.0.la \
	$(DEP_LIBS)			\
	$(TESTS_LIBS)

TEST_PROGS += test-completion
test_completion_SOURCES = test-completion.c
test_completion_LDADD = 		\
	$(top_builddir)/gtksourceview/libgtksourceview-2.0.la \
	$(DEP_LIBS)			\
	$(TESTS_LIBS)

UNIT_TEST_PROGS = test-languagemanager
test_languagemanager_SOURCES =		\
	test-languagemanager.c
test_languagemanager_LDADD = 		\
	$(top_builddir)/gtksourceview/libgtksourceview-2.0.la \
	$(DEP_LIBS)			\
	$(TESTS_LIBS)

UNIT_TEST_PROGS += test-printcompositor
test_printcompositor_SOURCES =		\
	test-printcompositor.c
test_printcompositor_LDADD = 		\
	$(top_builddir)/gtksourceview/libgtksourceview-2.0.la \
	$(DEP_LIBS)			\
	$(TESTS_LIBS)

# testregion need gtk_text_region_ api which is normally private
# modify gtksourceview/Makefile.am to export gtk_text_* symbols
# TEST_PROGS += testregion
#testregion_SOURCES = testregion.c
#testregion_LDADD = 			\
#	$(top_builddir)/gtksourceview/libgtksourceview-2.0.la \
#	$(DEP_LIBS)

EXTRA_DIST =				\
	apple-red.png			\
	gnome-gmush.png

-include $(top_srcdir)/git.mk

noinst_LTLIBRARIES = libshell-unpatched.la

INCLUDES = 							\
	$(CONTROL_CFLAGS)					\
	-I$(top_srcdir)/src

MARSHAL_FILES = cc-shell-marshal.c cc-shell-marshal.h
BUILT_SOURCES = $(MARSHAL_FILES)

cc-shell-marshal.h: cc-shell-marshal.list
	$(AM_V_GEN) $(GLIB_GENMARSHAL) --prefix=cc_shell_marshal $< --header > $@

cc-shell-marshal.c: cc-shell-marshal.list
	$(AM_V_GEN) $(GLIB_GENMARSHAL) --prefix=cc_shell_marshal $< --body --header > $@

libshell_unpatched_la_SOURCES =			\
	cc-shell-log.c				\
	cc-shell-log.h				\
	gnome-control-center.h			\
	cc-shell-category-view.c		\
	cc-shell-category-view.h		\
	cc-shell-item-view.c			\
	cc-shell-item-view.h			\
	cc-shell-model.c			\
	cc-shell-model.h			\
        cc-editable-entry.c			\
        cc-editable-entry.h			\
        cc-panel.c				\
        cc-panel.h				\
        cc-shell.c				\
        cc-shell.h				\
	$(MARSHAL_FILES)

EXTRA_DIST =					\
	cc-shell-marshal.list

bin_SCRIPTS = gnome-books

do_subst = sed -e 's|@abs_top_srcdir[@]|$(abs_top_srcdir)|g' \
               -e 's|@abs_top_builddir[@]|$(abs_top_builddir)|g' \
               -e 's|@localedir[@]|$(localedir)|g' \
               -e 's|@bindir[@]|$(bindir)|g' \
               -e 's|@libdir[@]|$(libdir)|g' \
               -e 's|@libexecdir[@]|$(libexecdir)|g' \
               -e 's|@pkglibdir[@]|$(pkglibdir)|g' \
               -e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
               -e 's|@GJS_CONSOLE[@]|$(GJS_CONSOLE)|g' \
               -e 's|@PACKAGE_NAME[@]|$(PACKAGE_NAME)|g' \
               -e 's|@PACKAGE_VERSION[@]|$(PACKAGE_VERSION)|g' \
               -e 's|@GETTEXT_PACKAGE[@]|$(GETTEXT_PACKAGE)|g'

gnome-books: gnome-books.in
	$(AM_V_GEN) $(do_subst) $< > $@
	chmod +x $@

jsdir = $(pkgdatadir)/js/
dist_js_DATA = 			\
	application.js  	\
        detailsWindow.js        \
	main.js  		\
	mainWindow.js 		\
	workModel.js 

CLEANFILES = \
    gnome-books
EXTRA_DIST = \
    gnome-books.in

SUBDIRS = pixmaps icons

@INTLTOOL_DESKTOP_RULE@

DESKTOP_IN_FILES= eom.desktop.in.in
DESKTOP_FILES= $(DESKTOP_IN_FILES:.desktop.in.in=.desktop)

desktopdir = $(datadir)/applications
desktop_DATA = $(DESKTOP_FILES)

@INTLTOOL_XML_RULE@
appdatadir = $(datadir)/metainfo
appdata_in_files = eom.appdata.xml.in
appdata_DATA = $(appdata_in_files:.xml.in=.xml)

gsettings_ENUM_NAMESPACE = org.mate.eom
gsettings_ENUM_FILES = $(top_srcdir)/src/eom-scroll-view.h	\
                       $(top_srcdir)/src/eom-window.h

gsettings_SCHEMAS = org.mate.eom.gschema.xml
@GSETTINGS_RULES@

uidir = $(pkgdatadir)
ui_DATA = \
	eom-toolbar.xml

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = eom.pc

EXTRA_DIST = \
	$(ui_DATA) \
	eom.css			\
	eom-image-properties-dialog.ui	\
	eom-multiple-save-as-dialog.ui	\
	eom-preferences-dialog.ui \
	eom-ui.xml		\
	metadata-sidebar.ui	\
	eom.about		\
	$(DESKTOP_IN_FILES) \
	$(appdata_in_files)

CLEANFILES = \
        $(appdata_DATA)

DISTCLEANFILES = \
        $(DESKTOP_FILES) \
        $(gsettings_SCHEMAS)

-include $(top_srcdir)/git.mk

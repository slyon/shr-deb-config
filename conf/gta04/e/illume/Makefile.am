MAINTAINERCLEANFILES = Makefile.in

EXTRA_DIST = \
        profile.desktop \
        icon.png \
        e.src \
        module.illume-home.src \
        module.illume-keyboard.src \
        module.illume-indicator.src \
        module.illume2.src

filesdir = /gta04/$(datadir)/enlightenment/data/config/shr
files_DATA = \
        profile.desktop \
        icon.png \
        e.cfg \
        module.illume-home.cfg \
        module.illume-keyboard.cfg \
        module.illume-indicator.cfg \
        module.illume2.cfg

SUFFIXES = .cfg

.src.cfg:
	$(EET) -e \
	$(top_builddir)/conf/gta04/e/illume/$@ conf/gta04/e/illume \
	$< 1

clean-local:
	rm -rf *.cfg *~

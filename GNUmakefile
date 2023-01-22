DESTDIR =
PREFIX  =/usr/local


all:
clean:
install:
update:
## -- install-sh --
install: install-sh
install-sh:
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	cp bin/gettar-create    $(DESTDIR)$(PREFIX)/bin
	cp bin/gettar           $(DESTDIR)$(PREFIX)/bin
	cp bin/gettar-tmpdir    $(DESTDIR)$(PREFIX)/bin
## -- install-sh --
## -- license --
install: install-license
install-license: LICENSE
	mkdir -p $(DESTDIR)$(PREFIX)/share/doc/sh-packaging
	cp LICENSE $(DESTDIR)$(PREFIX)/share/doc/sh-packaging
## -- license --

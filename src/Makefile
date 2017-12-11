PREFIX	  ?= /usr/local
BINPREFIX ?= $(PREFIX)/bin
LIBPREFIX ?= $(PREFIX)/lib
MANPREFIX ?= $(PREFIX)/share/man
DOCPREFIX ?= $(PREFIX)/share/doc
ETCPREFIX ?= /etc
VARPREFIX ?= /var
DESTDIR   ?=

all:		build-main install-main clean-main
build:		build-main
clean:		clean-main
install:	install-main
uninstall:	uninstall-main

build-main:
	mkdir -p ./cpp/build
	g++ -fopenmp --std=c++14 -x c++ -o ./cpp/build/emoss ./cpp/emoss.cpp -pg

clean-main:
	$(RM) ./cpp/build/emoss

install-main:
	install ./cpp/build/emoss $(BINPREFIX)/emoss

uninstall-main:
	$(RM) $(BINPREFIX)/emoss

.PHONY: all build clean install uninstall

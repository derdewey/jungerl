
include ../../../support/include.mk

include ../vsn.mk
VSN=$(DHCP_VSN)

DEBUG=

DOCDIR=`pwd`

ERL=erl
ERLC=erlc
ERLC_FLAGS+=-W $(DEBUG)
EMULATOR=beam


MODULES = dhcp_cli_srv dhcp_lib dhcp_test

EBIN = ../ebin
EBIN_FILES = $(MODULES:%=$(EBIN)/%.$(EMULATOR)) $(EBIN)/dhcp.app

all: $(EBIN_FILES)

debug:
	$(MAKE) DEBUG=-DDEBUG
clean:
	rm -rf $(EBIN_FILES)

dhcp_cli_srv.erl: ../include/dhcp_lib.hrl
dhcp_lib.erl: ../include/dhcp_lib.hrl
dhcp_test.erl: ../include/dhcp_lib.hrl
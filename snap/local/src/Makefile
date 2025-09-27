#!/usr/bin/make -f

SRC_DIR ?= .

DEST_LAUNCHER = desktop-launch

arch_triplet := $(shell dpkg-architecture -q DEB_TARGET_MULTIARCH)


build: $(DEST_LAUNCHER)

clean:
	rm -f $(DEST_LAUNCHER)

desktop-launch:
	@echo "#!/bin/bash" > $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/init >> $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/desktop-exports >> $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/launcher-specific >> $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/mark-and-exec >> $(DEST_LAUNCHER)

install: desktop-launch
	install -D -m755 $(DEST_LAUNCHER) "$(DESTDIR)"/bin/$(DEST_LAUNCHER)

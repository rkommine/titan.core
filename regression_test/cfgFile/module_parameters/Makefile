###############################################################################
# Copyright (c) 2000-2015 Ericsson Telecom AB
# All rights reserved. This program and the accompanying materials
# are made available under the terms of the Eclipse Public License v1.0
# which accompanies this distribution, and is available at
# http://www.eclipse.org/legal/epl-v10.html
###############################################################################
TOPDIR := ../../
include $(TOPDIR)/Makefile.regression
unexport ABS_SRC
unexport SRCDIR

DIRS := assignment concat references

# List of fake targets:
.PHONY: all dep clean run $(DIRS) $(addsuffix /, $(DIRS)) profile

all dep clean distclean run:
	for dir in $(DIRS); do $(MAKE) -C $$dir $@ || exit; done

# To run just one test, type "make dir" or "make "dir/"
$(DIRS) $(addsuffix /, $(DIRS)):
	$(MAKE) -C $@ run

# To run all tests, possibly in parallel
runall: $(DIRS)



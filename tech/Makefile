#
# qflow project tech makefile
#

# Main compiler arguments
CFLAGS = -g -O2
DEFS = -DPACKAGE_NAME=\"\" -DPACKAGE_TARNAME=\"\" -DPACKAGE_VERSION=\"\" -DPACKAGE_STRING=\"\" -DPACKAGE_BUGREPORT=\"\" -DPACKAGE_URL=\"\" -DSTDC_HEADERS=1 -DHAVE_SETENV=1 -DHAVE_PUTENV=1 -DTCLSH_PATH=\"/usr/bin/tclsh\" -DQFLOW_MAGIC_PATH=\"/usr/bin/magic\" -DQFLOW_QROUTER_PATH=\"/usr/bin/qrouter\" -DQFLOW_GRAYWOLF_PATH=\"/usr/bin/graywolf\" -DQFLOW_YOSYS_PATH=\"/usr/bin/yosys\"
LIBS = 
LDFLAGS = 
INSTALL = /usr/bin/install -c

QFLOW_LIB_DIR = /usr/share/qflow

TECH_DIRS = osu050 osu035 osu018

TECHINSTALL = ${QFLOW_LIB_DIR}/tech

all:
	@echo "Making all in tech directories"
	for target in $(TECH_DIRS); do \
	   (cd $$target ; $(MAKE) all) ;\
	done

install:
	@echo "Installing built-in tech files"
	$(INSTALL) -d $(DESTDIR)${TECHINSTALL}
	for target in $(TECH_DIRS); do \
	   (cd $$target ; $(MAKE) install) ;\
	done

clean:
	@echo "Cleaning up built-in tech files"
	for target in $(TECH_DIRS); do \
	   (cd $$target ; $(MAKE) clean) ;\
	done


uninstall:
	@echo "Uninstalling built-in tech files
	$(RM) -rf ${TECHINSTALL}


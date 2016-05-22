#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2016 Denys Rtveliashvili.  All rights reserved.
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		libvirt
COMPONENT_VERSION=	1.3.4
COMPONENT_FMRI=		system/library/libvirt
COMPONENT_CLASSIFICATION=System/Virtualization
COMPONENT_PROJECT_URL=	https://libvirt.org/
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_NAME)-$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:e2396ebebb3f3fdb50429ce8faa99559f6e8e3cc0493d5fa0c1999db189c25bd
COMPONENT_ARCHIVE_URL=	ftp://libvirt.org/libvirt/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=	"GNU Lesser General Public License"
COMPONENT_LICENSE_FILE=	$(COMPONENT_NAME).license
COMPONENT_SUMMARY=      A parser for HTTP mess

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

CONFIGURE_ENV += MAKE=$(GMAKE)
CONFIGURE_ENV += PATH="$(GNUBIN):$(PATH)"
COMPONENT_ENV += CC="$(CC)"
COMPONENT_ENV += CFLAGS="$(CC_BITS)"
COMPONENT_ENV += LDFLAGS="$(LD_BITS)"
#CONFIGURE_SCRIPT = $(SOURCE_DIR)/autogen.sh
CONFIGURE_SCRIPT = $(SOURCE_DIR)/configure
CONFIGURE_OPTIONS = --without-sasl --without-xen --without-qemu --without-vmware --without-esx --without-avahi --without-vbox --without-firewalld
MAKE=gmake

build:		$(BUILD_64)

install:	$(INSTALL_64)

test:		$(TEST_64)


#
# CDDL HEADER START
#
# The contents of this file are subject to the terms of the
# Common Development and Distribution License (the "License").
# You may not use this file except in compliance with the License.
#
# You can obtain a copy of the license at usr/src/OPENSOLARIS.LICENSE
# or http://www.opensolaris.org/os/licensing.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# When distributing Covered Code, include this CDDL HEADER in each
# file and include the License file at usr/src/OPENSOLARIS.LICENSE.
# If applicable, add the following below this CDDL HEADER, with the
# fields enclosed by brackets "[]" replaced with your own identifying
# information: Portions Copyright [yyyy] [name of copyright owner]
#
# CDDL HEADER END
#
# Copyright 2011 EveryCity Ltd. All rights reserved.
# Copyright 2013, Jon Tibble.  All rights reserved.
#
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		mbuffer
COMPONENT_VERSION=	20160228
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tgz
COMPONENT_ARCHIVE_HASH=	sha256:f7769f729e9b26a22a5d91922a740a0d1df6004dbe2b7a1febb0d7e4c3ef9e62
COMPONENT_ARCHIVE_URL=	http://www.maier-komor.de/software/mbuffer/$(COMPONENT_ARCHIVE)

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

build:		$(BUILD_32_and_64)

install:	$(INSTALL_32_and_64)

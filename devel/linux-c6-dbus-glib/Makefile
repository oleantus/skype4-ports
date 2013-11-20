# Created by: bsam
# $FreeBSD: head/devel/linux-f10-dbus-glib/Makefile 329552 2013-10-06 12:19:41Z rene $

PORTNAME=	dbus-glib
PORTVERSION=	0.86
RPMVERSION=	5.el6
USE_LINUX=	c6

CATEGORIES=	devel linux
MAINTAINER=	emulation@FreeBSD.org
COMMENT=	GLib bindings for D-Bus (Linux Fedora ${LINUX_DIST_VER})

PKGNAMEPREFIX=	linux-${USE_LINUX}-
MASTER_SITES=	http://vault.centos.org/${LINUX_DIST_VER}/os/i386/Packages/
DISTNAME=	${PORTNAME}-${PORTVERSION}-${RPMVERSION}
DIST_SUBDIR=	rpm/${LINUX_RPM_ARCH}/centos/${LINUX_DIST_VER}

ONLY_FOR_ARCHS=	i386 amd64

USE_LINUX_RPM=	yes
USE_LINUX_APPS=	dbuslibs expat
LINUX_RPM_ARCH=	i686
LINUX_DIST_VER=	6.2
BRANDELF_FILES=	usr/bin/dbus-binding-tool
USE_LDCONFIG=	yes

PLIST_FILES=	usr/bin/dbus-binding-tool usr/lib/libdbus-glib-1.so.2 \
		usr/lib/libdbus-glib-1.so.2.1.0
DOCSDIR=	usr/share/doc/dbus-glib-${PORTVERSION}
PORTDOCS=	COPYING ChangeLog NEWS
DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr

CONFLICTS=	linux-dbus-glib-[0-9]*  linux-f10-dbus-glib-[0-9]*

.include <bsd.port.mk>

# Created by: Artyom Mirgorodskiy <artyom.mirgorodsky@gmail.com>
# $FreeBSD$

PORTNAME=	nss
PORTVERSION=	3.12.10
RPMVERSION=	16.el6
USE_LINUX=	c6
USE_LINUX_APPS=	nspr sqlite3

CATEGORIES=	security linux
MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Network Security Services (Linux CentOS 6)

DISTFILES=	${PORTNAME}-${PORTVERSION}-${RPMVERSION}.${LINUX_RPM_ARCH}.rpm \
		nss-util-3.12.10-2.el6.${LINUX_RPM_ARCH}.rpm \
		nss-softokn-3.12.9-11.el6.${LINUX_RPM_ARCH}.rpm \
		nss-softokn-freebl-3.12.9-11.el6.${LINUX_RPM_ARCH}.rpm

PKGNAMEPREFIX=	linux-${USE_LINUX}-
DISTNAME=	${PORTNAME}-${PORTVERSION}-${RPMVERSION}

CONFLICTS=	linux-f10-nss-[0-9]*

ONLY_FOR_ARCHS=	i386 amd64
USE_LINUX_RPM=	yes
LINUX_RPM_ARCH=		i686
USE_LDCONFIG=	yes

DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr

.include <bsd.port.mk>

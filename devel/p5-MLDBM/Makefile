# $FabBSD$
# $OpenBSD: Makefile,v 1.12 2007/09/16 02:53:07 merdely Exp $

COMMENT=	store multi-level hash structure in single-level tied hash

MODULES=	cpan
DISTNAME=	MLDBM-2.01
PKGNAME=	p5-${DISTNAME}p1
CATEGORIES=	devel

RUN_DEPENDS=	:p5-FreezeThaw->=0.3:devel/p5-FreezeThaw
BUILD_DEPENDS=	${RUN_DEPENDS}

PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

.include <bsd.port.mk>

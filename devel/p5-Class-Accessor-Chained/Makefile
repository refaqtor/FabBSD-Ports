# $FabBSD$
# $OpenBSD: Makefile,v 1.4 2007/09/16 02:53:03 merdely Exp $

COMMENT=		make chained accessors

MODULES=		cpan
DISTNAME=		Class-Accessor-Chained-0.01
CATEGORIES=		devel

# From OpenBSD:
#MAINTAINER=		Sean Comeau <scomeau@obscurity.org>

# Artistic
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

RUN_DEPENDS=		::devel/p5-Class-Accessor
BUILD_DEPENDS=		${RUN_DEPENDS}

.include <bsd.port.mk>

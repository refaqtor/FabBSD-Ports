# $FabBSD$
# $OpenBSD: Makefile,v 1.14 2007/09/16 01:40:28 merdely Exp $

SHARED_ONLY=	Yes

COMMENT=	module to implement efficient mapping tables

DISTNAME=	Unicode-Map8-0.12
CATEGORIES=	converters
MODULES=	cpan

# From OpenBSD:
#MAINTAINER=	Kevin Lo <kevlo@openbsd.org>

# Perl
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

RUN_DEPENDS=	::converters/p5-Unicode-String

.include <bsd.port.mk>

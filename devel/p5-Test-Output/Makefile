# $FabBSD$
# $OpenBSD: Makefile,v 1.2 2007/09/16 02:53:09 merdely Exp $

COMMENT= 	test output of other modules

MODULES=	cpan
DISTNAME=	Test-Output-0.10
CATEGORIES=	devel

# perl
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

RUN_DEPENDS=		::devel/p5-Sub-Exporter

REGRESS_DEPENDS=	::devel/p5-Test-Tester

MAKE_ENV=		TEST_POD=Yes
.include <bsd.port.mk>

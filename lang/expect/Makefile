# $FabBSD$
# $OpenBSD: Makefile,v 1.48 2007/09/16 00:27:05 merdely Exp $

COMMENT=	sophisticated scripter based on Tcl/Tk

DISTNAME=	expect-5.43.0
PKGNAME=	${DISTNAME}p0
SHARED_LIBS=	expect543 1.2
CATEGORIES=	lang
MASTER_SITES=	http://expect.nist.gov/old/

HOMEPAGE=	http://expect.nist.gov/

# PD
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes
WANTLIB=		c util m

LIB_DEPENDS+=	tcl84:tcl-8.4.*:lang/tcl/8.4

SEPARATE_BUILD=	concurrent
CONFIGURE_STYLE=gnu
CONFIGURE_ARGS+=${CONFIGURE_SHARED}
CONFIGURE_ARGS+=--with-tclconfig="${LOCALBASE}/lib/tcl8.4"\
		--with-tclinclude="${LOCALBASE}/include/tcl8.4"
CONFIGURE_ENV=	LIBexpect543_VERSION=${LIBexpect543_VERSION}

REGRESS_TARGET=	test

DESTDIRNAME=	INSTALL_ROOT

WRKDIST=	${WRKDIR}/expect-5.43

.include <bsd.port.mk>

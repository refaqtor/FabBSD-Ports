# $FabBSD$
# $OpenBSD: Makefile,v 1.29 2008/07/06 21:25:25 jasper Exp $

COMMENT=	perl-compatible regular expression library

DISTNAME=	pcre-7.7
PKGNAME=	${DISTNAME}p0

SHARED_LIBS=	pcre		2.2 \
		pcrecpp		3.1 \
		pcreposix	1.4

CATEGORIES=	devel

MASTER_SITES=	ftp://ftp.csx.cam.ac.uk/pub/software/programming/pcre/ \
		${MASTER_SITE_SOURCEFORGE:=pcre/}

HOMEPAGE=	http://www.pcre.org/

# From OpenBSD:
# MAINTAINER=	Jakob Schlyter <jakob@openbsd.org>

# BSD
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes
WANTLIB=		c

USE_LIBTOOL=		Yes
CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS=		${CONFIGURE_SHARED} \
			--enable-utf8 \
			--enable-unicode-properties

.include <bsd.port.mk>

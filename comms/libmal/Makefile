# $FabBSD$
# $OpenBSD: Makefile,v 1.6 2007/09/16 01:37:09 merdely Exp $

COMMENT=	MAL convenience library

DISTNAME=	libmal-0.44
SHARED_LIBS +=	mal 1.0				# .1.0
CATEGORIES=	comms palm

HOMEPAGE=	http://jasonday.home.att.net/code/libmal/

# From OpenBSD:
#MAINTAINER=	Antoine Jacoutot <ajacoutot@openbsd.org>

# MPL
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM= Yes
PERMIT_DISTFILES_FTP=	Yes

MASTER_SITES=	${HOMEPAGE}

WANTLIB=	c pthread

LIB_DEPENDS=	pisock.>=9::comms/pilot-link

USE_LIBTOOL=	Yes
CONFIGURE_STYLE=gnu

MAKE_FLAGS+=	CFLAGS="${CFLAGS} -pthread"
CONFIGURE_ARGS=	${CONFIGURE_SHARED}

.include <bsd.port.mk>

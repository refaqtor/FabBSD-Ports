# $FabBSD$
# $OpenBSD: Makefile,v 1.4 2007/09/15 21:17:24 merdely Exp $

COMMENT=		Perl shell

DISTNAME=		psh-1.8
PKGNAME=		${DISTNAME:S/p/perl/}p1
CATEGORIES=		shells

HOMEPAGE=		http://www.focusresearch.com/gregor/sw/psh/

# From OpenBSD:
#MAINTAINER=		Jasper Lievisse Adriaanse <jasper@openbsd.org>

# GPL
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

MASTER_SITES=		http://www.focusresearch.com/gregor/download/

RUN_DEPENDS=		::devel/p5-Term-ReadLine-Gnu \
			::devel/p5-BSD-Resource

CONFIGURE_STYLE=	perl

PKG_ARCH=		*

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/psh/themes
	${INSTALL_DATA_DIR} ${PREFIX}/share/psh/complete
	${INSTALL_DATA} ${WRKSRC}/share/themes/* ${PREFIX}/share/psh/themes
	${INSTALL_DATA} ${WRKSRC}/share/complete/* ${PREFIX}/share/psh/complete

.include <bsd.port.mk>

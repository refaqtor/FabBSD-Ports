# $FabBSD$
# $OpenBSD: Makefile,v 1.3 2007/09/16 02:52:57 merdely Exp $

COMMENT=	Atmel AVR 8-bit RISC microcontrollers' GNU binutils

VER=		2.15
DISTNAME=	binutils-${VER}
PKGNAME=	avr-binutils-${VER}p0
EXTRACT_SUFX=	.tar.bz2

HOMEPAGE=	http://www.gnu.org/software/binutils/

# GPL
PERMIT_PACKAGE_CDROM=   Yes
PERMIT_PACKAGE_FTP=     Yes
PERMIT_DISTFILES_CDROM= Yes
PERMIT_DISTFILES_FTP=   Yes
WANTLIB=		c

MASTER_SITES=	${MASTER_SITE_GNU:=binutils/}

CONFIGURE_ARGS+=--enable-commonbfdlib=no

USE_LIBTOOL=	Yes
LIBTOOL_FLAGS=	--tag=disable-shared

.include <bsd.port.mk>

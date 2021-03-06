# $FabBSD$
# $OpenBSD: Makefile,v 1.3 2008/04/27 13:47:15 sthen Exp $

COMMENT=	Tool Command Language

VERSION=	8.5.2

DISTNAME=	tcl${VERSION}
PKGNAME=	tcl-${VERSION}p1
SHARED_LIBS=	tcl85 0.0
CATEGORIES=	lang lang/tcl
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=tcl/}
DISTFILES=	tcl${VERSION}-src.tar.gz
WANTLIB=	c m

# From OpenBSD:
#MAINTAINER=	Stuart Cassoff <stwo@users.sourceforge.net>
HOMEPAGE=	http://www.tcl.tk/

# BSD
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

FLAVORS=	threaded
FLAVOR?=

WRKSRC=		${WRKDIST}/unix

SEPARATE_BUILD=	concurrent
AUTOCONF_VERSION= 2.59
CONFIGURE_STYLE= autoconf no-autoheader old
CONFIGURE_ARGS=	${CONFIGURE_SHARED} \
		--includedir="${LOCALBASE}/include/tcl8.5" \
		--mandir="${LOCALBASE}/lib/tcl8.5/man" \
		--sysconfdir="${SYSCONFDIR}"

CONFIGURE_ENV=	LIBtcl85_VERSION=${LIBtcl85_VERSION}
CONFIGURE_ENV+= CFLAGS=""

FAKE_FLAGS=	INSTALL_DATA_DIR="${INSTALL_DATA_DIR}"\
		INSTALL_LIBRARY="${INSTALL_DATA}" \
		INSTALL_DATA="${INSTALL_DATA}"

FAKE_FLAGS+=INSTALL_PROGRAM="${INSTALL_PROGRAM}"

.if ${FLAVOR:L:Mthreaded}
CONFIGURE_ARGS+=--enable-threads
WANTLIB+=pthread
.endif

# Needs a full network connection to run?
#REGRESS_IS_INTERACTIVE=Yes
REGRESS_TARGET=	test
REGRESS_FLAGS=	HOME=${TESTHOME}
TESTHOME=${WRKDIR}/testhome

pre-regress:
	@mkdir -p ${TESTHOME}

post-install:
	ln -s libtclstub85.a ${PREFIX}/lib/libtclstub85_pic.a

.include <bsd.port.mk>

# $FabBSD$
# $OpenBSD: Makefile,v 1.5 2008/07/04 19:57:06 naddy Exp $

SHARED_ONLY=	Yes

COMMENT=	access a MySQL database from Ruby

VERSION=	2.7.5
DISTNAME=	mysql-ruby-${VERSION}
PKGNAME=	ruby-mysql-${VERSION}p1
CATEGORIES=	databases

HOMEPAGE=	http://tmtm.org/mysql/ruby/

# Ruby License
PERMIT_PACKAGE_CDROM=	Yes
PERMIT_PACKAGE_FTP=	Yes
PERMIT_DISTFILES_CDROM=	Yes
PERMIT_DISTFILES_FTP=	Yes

MASTER_SITES=	${MASTER_SITE_RUBYFORGE:=mysql-ruby/}

MODULES=	lang/ruby

WANTLIB=	c m

LIB_DEPENDS=	mysqlclient::databases/mysql \
		ruby::lang/ruby

CONFIGURE_STYLE=ruby extconf

REGRESS_DEPENDS=::databases/mysql,-server

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ruby-mysql
	${INSTALL_DATA} ${WRKBUILD}/README.html ${PREFIX}/share/doc/ruby-mysql
	${INSTALL_DATA} ${WRKBUILD}/tommy.css ${PREFIX}/share/doc/ruby-mysql

# A running mysqld is required to run the regression tests.
do-regress:
	@cd ${WRKBUILD} && ${RUBY} test.rb

.include <bsd.port.mk>

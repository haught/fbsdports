# Created by: Gea-Suan Lin <gslin@gslin.org>
# $FreeBSD: head/databases/pecl-memcached/Makefile 381874 2015-03-21 22:00:31Z sunpoet $

PORTNAME=	memcached
PORTVERSION=	2.2.0
PORTREVISION=	9
CATEGORIES=	databases
MASTER_SITES=	http://pecl.php.net/get/
PKGNAMEPREFIX=	pecl-
DIST_SUBDIR=	PECL

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	PHP extension for interfacing with memcached via libmemcached library

LICENSE=	PHP30

LIB_DEPENDS=	libmemcached.so:${PORTSDIR}/databases/libmemcached

OPTIONS_DEFINE=	IGBINARY SASL
IGBINARY_DESC=	Binary serializer support

CONFIGURE_ARGS=	--disable-memcached-sasl --with-libmemcached-dir=${LOCALBASE}
USE_PHP=	json:build session:build
USE_PHPEXT=	yes
USE_PHPIZE=	yes
USE_PHP_BUILD=	yes
USES=		php:ext pkgconfig tar:tgz
USE_GITHUB=	yes
GH_ACCOUNT=	php-memcached-dev
GH_PROJECT=	php-memcached
GH_TAGNAME=	a8ed24065cb1f2daf84308bf3ddf7a1d528d3ef5

IGBINARY_CONFIGURE_ENABLE=	memcached-igbinary
IGBINARY_USE=		PHP=igbinary
SASL_CONFIGURE_ENABLE=	memcached-sasl
SASL_LIB_DEPENDS=	libsasl2.so:${PORTSDIR}/security/cyrus-sasl2

.include <bsd.port.mk>

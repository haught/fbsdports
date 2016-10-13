# $FreeBSD$

PORTNAME=	fluent-mixin-config-placeholders
PORTVERSION=	0.4.0
CATEGORIES=	sysutils rubygems
MASTER_SITES=	RG

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Fluent plugin which provide some placeholders to fluentd \
		plugins that includes this mix-in.

RUN_DEPENDS=	\
	rubygem-fluentd>0:${PORTSDIR}/sysutils/rubygem-fluentd \
	rubygem-uuidtools>=2.1.5:${PORTSDIR}/devel/rubygem-uuidtools

USE_RUBY=	yes
USES=           gem

.include <bsd.port.mk>

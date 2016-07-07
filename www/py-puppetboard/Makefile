# $FreeBSD$

PORTNAME=	puppetboard
PORTVERSION=	0.2.0
DISTVERSIONPREFIX=	v
CATEGORIES=	www python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	allanjude@FreeBSD.org
COMMENT=	Web interface to PuppetDB

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}Flask>=0.10.1:www/py-flask \
		${PYTHON_PKGNAMEPREFIX}Flask-WTF>=0.12:www/py-flask-wtf \
		${PYTHON_PKGNAMEPREFIX}Jinja2>=2.7.2:devel/py-Jinja2 \
		${PYTHON_PKGNAMEPREFIX}MarkupSafe>=0.19:textproc/py-MarkupSafe \
		${PYTHON_PKGNAMEPREFIX}wtforms>=2.1:textproc/py-wtforms \
		${PYTHON_PKGNAMEPREFIX}werkzeug>=0.11.10:www/py-werkzeug \
		${PYTHON_PKGNAMEPREFIX}itsdangerous>=0.23:security/py-itsdangerous \
		${PYTHON_PKGNAMEPREFIX}pypuppetdb>=0.3.1:databases/py-pypuppetdb \
		${PYTHON_PKGNAMEPREFIX}requests>=2.6.0:www/py-requests

USE_GITHUB=	yes
GH_ACCOUNT=	puppet-community

USES=		python:2.7
USE_PYTHON=	autoplist distutils

PLIST_FILES=	"@sample etc/puppetboard/default_settings.py.sample"

post-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/etc/puppetboard
	${CP} ${WRKSRC}/puppetboard/default_settings.py ${STAGEDIR}${PREFIX}/etc/puppetboard/default_settings.py.sample

.include <bsd.port.mk>

# $FreeBSD$

PORTNAME=	xf86-video-ati-legacy
PORTVERSION=	7.9.0
PORTREVISION=	4
PORTEPOCH=	1
CATEGORIES=	x11-drivers
DISTNAME=	xf86-video-ati-${DISTVERSION}

MAINTAINER=	x11@FreeBSD.org
COMMENT=	X.Org ati display driver

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		does not build with xorg-server 1.20.7

# No Radeon kernel driver on non-x86 and PC98.
ONLY_FOR_ARCHS=		amd64 i386 powerpc64
ONLY_FOR_ARCHS_REASON=	KMS is required and currently only available on x86

LIB_DEPENDS=	libpciaccess.so:devel/libpciaccess \
		libdrm_radeon.so:graphics/libdrm

CONFLICTS_INSTALL=	xf86-video-ati

PORTSCOUT=	limit:^7\.9\.0

USES=		gl xorg xorg-cat:driver
USE_GL=		gl
USE_XORG=	pciaccess

CONFIGURE_ARGS+=--disable-udev

.include <bsd.port.mk>

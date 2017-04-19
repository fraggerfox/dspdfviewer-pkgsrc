# $NetBSD$

VERSION=        1.15.1
GITHUB_PROJECT=	dspdfviewer
GITHUB_ACCOUNT=	dannyedel
GITHUB_TAG=	v${VERSION}
DISTNAME=	${GITHUB_PROJECT}-${VERSION}
CATEGORIES=	print
MASTER_SITES=	${MASTER_SITE_GITHUB:=${GITHUB_ACCOUNT}/}

MAINTAINER=	santhosh.raju@gmail.com
HOMEPAGE=	http://dspdfviewer.danny-edel.de/
COMMENT=	Dual-Screen PDF Viewer for latex-beamer
LICENSE=	gnu-gpl-v2

WRKSRC=		${WRKDIR}/${DISTNAME}
CONFIGURE_DIR=	${WRKSRC}/build
BUILD_DIRS= 	build

USE_LANGUAGES=	c c++
USE_TOOLS+=	cmake pkg-config
USE_CMAKE=	yes
CMAKE_ARGS+=	-DBuildTests=OFF
CMAKE_ARG_PATH=	${WRKSRC}/build
BUILD_MAKE_FLAGS+= VERBOSE=1

DEPENDS+=	boost-libs>=1.63.0:../../devel/boost-libs
DEPENDS+=	poppler-qt5>=0.50.0:../../print/poppler-qt5
DEPENDS+=	qt5-qttools>=5.5.1:../../x11/qt5-qttools

INSTALL_MAN_DIR=	share/

pre-configure:
	mkdir -p ${WRKSRC}/build

do-configure:
	cd ${CONFIGURE_DIR} && cmake .. ${CMAKE_ARGS}

.include "../../devel/boost-libs/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../print/poppler-qt5/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"

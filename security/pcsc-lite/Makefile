# $OpenBSD: Makefile,v 1.52 2021/11/02 00:02:16 sthen Exp $

COMMENT=	resource manager for PC/SC

V=		1.9.5
REVISION=	2
DISTNAME=	pcsc-lite-${V}
CATEGORIES=	security

SHARED_LIBS+=	pcsclite	1.0 # 1.0.0
SHARED_LIBS+=	pcscspy		0.0 # 0.0.0

HOMEPAGE=	https://pcsclite.apdu.fr

MASTER_SITES=	https://pcsclite.apdu.fr/files/

EXTRACT_SUFX=	.tar.bz2

# BSD and GPLv3+
PERMIT_PACKAGE=	Yes

WANTLIB=		c pthread usb-1.0

MODULES+=		lang/python
MODPY_BUILDDEP=		No

MODPY_ADJ_LINES=	src/spy/pcsc-spy

# thread-local storage
COMPILER=		base-clang ports-gcc
COMPILER_LANGS=		c

LIB_DEPENDS=		devel/libusb1

MODPY_ADJ_FILES=	src/spy/pcsc-spy

USE_GMAKE=	Yes

CONFIGURE_STYLE= gnu

CONFIGURE_ARGS=	--disable-libudev \
		--disable-libsystemd \
		--without-systemdsystemunitdir \
		--enable-libusb \
		--runstatedir=/var/run \
		--enable-ipcdir=/var/run/pcscd \
		--enable-confdir=${SYSCONFDIR}/ccid

CONFIGURE_ENV=	ac_cv_lib_lex='none needed'

TEST_DEPENDS=	${BUILD_PKGPATH}=${V} \
		security/ccid

# The pcscd server needs to be up and running
TEST_IS_INTERACTIVE= Yes

do-test:
	${WRKBUILD}/src/testpcsc

.include <bsd.port.mk>

# $OpenBSD$

COMMENT =		libuv bindings for luajit and lua

VER =			1.30.1-1
PKGVER =		1.30.1.1
DISTNAME =		luv-${VER}
PKGNAME = 		libluv-${PKGVER}

SHARED_LIBS +=		luv 	0.0

CATEGORIES =		devel

HOMEPAGE =		https://github.com/luvit/luv

# Apache 2.0
PERMIT_PACKAGE =	Yes

MASTER_SITES =		${HOMEPAGE}/releases/download/${VER}/

MODULES +=		devel/cmake \
			lang/lua

WANTLIB +=		uv pthread

BUILD_DEPENDS =		devel/cmake \
			devel/libuv
		

LIB_DEPENDS =		devel/libuv

CONFIGURE_ARGS =	-DWITH_SHARED_LIBUV=ON \
					-DWITH_LUA_ENGINE=Lua \
					-DLUA_BUILD_TYPE=System \
					-DBUILD_MODULE=OFF \
					-DBUILD_SHARED_LIBS=ON \

NO_TEST =			YES

.include <bsd.port.mk>

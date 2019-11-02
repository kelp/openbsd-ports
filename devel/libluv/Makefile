# $OpenBSD$

COMMENT =		shared library of "luv" Lua bindings for libuv

VER =			1.30.1-1
DISTNAME =		luv-${VER}
PKGNAME =		libluv-${VER:S/-/./g}

SHARED_LIBS +=		luv 0.0

CATEGORIES =		devel

HOMEPAGE =		https://github.com/luvit/luv

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB +=		uv

MASTER_SITES =		${HOMEPAGE}/releases/download/${VER}/

MODULES +=		devel/cmake \
			lang/lua

BUILD_DEPENDS =		devel/lua-compat53

LIB_DEPENDS =		devel/libuv

CONFIGURE_ARGS =	-DWITH_SHARED_LIBUV=ON \
			-DWITH_LUA_ENGINE=Lua \
			-DLUA_BUILD_TYPE=System \
			-DBUILD_MODULE=OFF \
			-DBUILD_SHARED_LIBS=ON \

NO_TEST =		Yes

.include <bsd.port.mk>

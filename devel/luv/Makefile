# $OpenBSD$

COMMENT =		libuv bindings for LuaJIT and Lua

VER =			1.30.1-1
DISTNAME =		luv-${VER}
PKGNAME = 		luv-${VER:S/-/./g}

SHARED_LIBS +=		luv 0.0

CATEGORIES =		devel

HOMEPAGE =		https://github.com/luvit/luv

# Apache 2.0
PERMIT_PACKAGE =	Yes

MASTER_SITES =		${HOMEPAGE}/releases/download/${VER}/

MODULES +=		devel/cmake \
			lang/lua

WANTLIB +=		uv

BUILD_DEPENDS =		devel/cmake \
			devel/lua-compat53

LIB_DEPENDS =		devel/libuv

CONFIGURE_ARGS =	-DWITH_SHARED_LIBUV=ON \
			-DWITH_LUA_ENGINE=Lua \
			-DLUA_BUILD_TYPE=System \
			-DBUILD_MODULE=OFF \
			-DBUILD_SHARED_LIBS=ON \

NO_TEST =		YES
SEPARATE_BUILD =	YES

.include <bsd.port.mk>

# $OpenBSD$

COMMENT =		shared library of "luv" Lua bindings for libuv

VER =			1.32.0-0
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
			-DBUILD_MODULE=ON \
			-DBUILD_SHARED_LIBS=ON \
			-DWITH_LUA_ENGINE=Lua \
			-DLUA_BUILD_TYPE=System \
			-DINSTALL_LIB_DIR=${MODLUA_LIBDIR} \
			-DLUA_INCLUDE_DIR=${MODLUA_INCLUD_DIR}

NO_TEST =		Yes

.include <bsd.port.mk>

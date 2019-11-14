# $OpenBSD: Makefile,v 1.18 2019/07/09 09:46:16 edd Exp $

COMMENT =	continuation and extension of Vim

GH_ACCOUNT =	neovim
GH_PROJECT =	neovim
GH_TAGNAME =	v0.4.3

CATEGORIES =	editors devel
HOMEPAGE =	https://neovim.io
MAINTAINER =	Edd Barrett <edd@openbsd.org>

# Neovim must be statically linked with libluv because there isn't yet a
# libluv port.
LUV_VER    =	1.30.1-1
LUV	   =	luv-${LUV_VER}
MASTER_SITES0 = https://github.com/luvit/luv/releases/download/${LUV_VER}/
DISTFILES  =	${DISTNAME}${EXTRACT_SUFX} \
		${LUV}${EXTRACT_SUFX}:0

# Apache 2.0 + Vim License
PERMIT_PACKAGE =	Yes

WANTLIB += c iconv intl ${MODLUA_WANTLIB} m msgpackc pthread termkey
WANTLIB += unibilium util uv vterm

COMPILER =		base-clang ports-gcc base-gcc

MODULES =		devel/cmake \
			lang/lua \
			textproc/intltool

BUILD_DEPENDS =		${RUN_DEPENDS} \
			devel/gperf \
			devel/lpeg \
			devel/lua-bitop

LIB_DEPENDS =		devel/gettext,-runtime \
			devel/libtermkey \
			devel/libuv \
			devel/libvterm>=1.0 \
			devel/msgpack \
			devel/unibilium>=1.0

RUN_DEPENDS +=		devel/libmpack/lua \
			devel/libmpack/main \
			devel/desktop-file-utils

MAKE_FLAGS +=		USE_BUNDLED=OFF
CONFIGURE_ARGS +=	-DLUA_PRG=${MODLUA_BIN} \
			-DLUA_INCLUDE_DIR=${MODLUA_INCL_DIR} \
			-DLUA_LIBRARIES=${MODLUA_LIB} \
			-DLIBLUV_INCLUDE_DIR=${WRKBUILD}/deps/include \
			-DLIBLUV_LIBRARY=${WRKBUILD}/deps/lib/libluv.a \
			-DPREFER_LUA=ON # disables LuaJIT

# Tests need gmake
USE_GMAKE = Yes
# `test_startup_utf8.vim' requires either bash or zsh
TEST_DEPENDS =	shells/bash \
		editors/py-neovim \
		editors/py-neovim,python3

# Build libluv first as a static library. We opted not to create a libluv
# port because it must be built for a specific Lua version and we don't know
# what version future ports might need. Currently no other port requires
# libluv, so it's simpler to build a static library here.
pre-configure:
	@mkdir -p ${WRKBUILD}/build
	@(cd ${WRKBUILD}/build && \
		cmake -DWITH_LUA_ENGINE=Lua \
		-DLUA_LIBRARIES=${MODLUA_LIB} \
		-DLUA_INCLUDE_DIR=${MODLUA_INCL_DIR} -DBUILD_MODULE=OFF \
		-DLUA_BUILD_TYPE=System \
		-DCMAKE_INSTALL_PREFIX=${WRKBUILD}/deps ${WRKDIR}/${LUV} && \
		${MAKE} install)

# These are the "old tests". There is also a new suite, but we would need the
# "busted" test suite for Lua, which is not yet ported.
#
# There is currently one (minor) test failure:
# https://github.com/neovim/neovim/issues/10420
do-test:
	cd ${WRKSRC}/src/nvim/testdir && env LC_CTYPE=en_US.UTF-8 \
		${MAKE_PROGRAM} NVIM_PRG=${WRKBUILD}/bin/nvim ${MAKE_FLAGS}

.include <bsd.port.mk>

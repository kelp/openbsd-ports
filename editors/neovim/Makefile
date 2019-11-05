# $OpenBSD: Makefile,v 1.18 2019/07/09 09:46:16 edd Exp $

COMMENT =	continuation and extension of Vim

GH_ACCOUNT =	neovim
GH_PROJECT =	neovim
GH_TAGNAME =	v0.4.2

CATEGORIES =	editors devel
HOMEPAGE =	https://neovim.io
MAINTAINER =	Edd Barrett <edd@openbsd.org>

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
			-DUSE_BUNDLED_GPERF=Off \
			-DUSE_BUNDLED_UNIBILIUM=Off \
			-DUSE_BUNDLED_LIBTERMKEY=Off \
			-DUSE_BUNDLED_LIBVTERM=Off \
			-DUSE_BUNDLED_LIBUV=Off \
			-DUSE_BUNDLED_MSGPACK=Off \
			-DUSE_BUNDLED_LUAJIT=Off \
			-DUSE_BUNDLED_LUAROCKS=Off \
			-DUSE_BUNDLED_LUV=On \
			-DLIBLUV_INCLUDE_DIR=${WRKBUILD}/.deps/usr/include \
			-DLIBLUV_LIBRARY=${WRKBUILD}/.deps/usr/lib/libluv.a \
			-DPREFER_LUA=ON # disables LuaJIT

# Tests need gmake
USE_GMAKE = Yes
# `test_startup_utf8.vim' requires either bash or zsh
TEST_DEPENDS =	shells/bash \
		editors/py-neovim \
		editors/py-neovim,python3

# Build third-party dependencies first for libluv. We opted not to create a 
# libluv port because it must be built for a specific Lua version and we don't
# know what version future ports might need. Currently no other port requires 
# libluv, so it's simpler to use the bundled library.
pre-configure:
	mkdir -p ${WRKBUILD}/.deps
	cd ${WRKBUILD}/.deps && cmake ${CONFIGURE_ARGS} ${WRKSRC}/third-party && \
		${MAKE_PROGRAM}

# These are the "old tests". There is also a new suite, but we would need the
# "busted" test suite for Lua, which is not yet ported.
#
# There is currently one (minor) test failure:
# https://github.com/neovim/neovim/issues/10420
do-test:
	cd ${WRKSRC}/src/nvim/testdir && env LC_CTYPE=en_US.UTF-8 \
		${MAKE_PROGRAM} NVIM_PRG=${WRKBUILD}/bin/nvim ${MAKE_FLAGS}

.include <bsd.port.mk>

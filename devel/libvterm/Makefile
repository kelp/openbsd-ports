# $OpenBSD$

COMMENT =	VT220/xterm/ECMA-48 terminal emulator library
# No releases, so use date and a git hash.
# Note that the github repo is a mirror of a bzr repo.
VERSION =	20190910
DISTNAME =	libvterm-${VERSION}

GH_ACCOUNT =	neovim
GH_PROJECT =	libvterm
# commit sha from the nvim branch
GH_COMMIT =	4a5fa43e0dbc0db4fe67d40d788d60852864df9e

SHARED_LIBS +=  vterm                     0.1 # 0.0

CATEGORIES =	devel

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB += c

USE_GMAKE =		Yes

.include <bsd.port.mk>

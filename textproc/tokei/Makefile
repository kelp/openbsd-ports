# $OpenBSD: $
#
COMMENT =		Tokei is a program that displays statistics about your code.

VER =			v10.0.1
DISTNAME =		tokei-${VER}

GH_ACCOUNT = 	XAMPPRocky
GH_PROJECT = 	tokei
GH_TAGNAME = 	${VER}

CATEGORIES =	textproc

# https preferred for HOMEPAGE
HOMEPAGE =		https://github.com/XAMPPRocky/tokei

PERMIT_PACKAGE =	Yes

# as devel/cargo MODULES adds DISTFILES, GH_* didn't
DISTFILES +=            ${DISTNAME}${EXTRACT_SUFX}

# "make port-lib-depends-check" can help
WANTLIB =		pthread c c++abi

# Any modules we may be using
MODULES =			devel/cargo

# Dependencies
#BUILD_DEPENDS =	???
#RUN_DEPENDS =		???
#LIB_DEPENDS =		???
#TEST_DEPENDS =		???

#MAKE_FLAGS =		???
#MAKE_ENV =		???
#FAKE_FLAGS =		???
#TEST_FLAGS =		???

# build/configuration variables
#
SEPARATE_BUILD =	Yes

MODCARGO_CRATES_UPDATE +=	libc

CONFIGURE_STYLE =	cargo

#RELEASE_DIR = 		${MODCARGO_TARGET_DIR}/release

MODCARGO_CRATES +=	aho-corasick	0.7.3
MODCARGO_CRATES +=	ansi_term	0.11.0
MODCARGO_CRATES +=	argon2rs	0.2.5
MODCARGO_CRATES +=	arrayvec	0.4.10
MODCARGO_CRATES +=	atty	0.2.11
MODCARGO_CRATES +=	autocfg	0.1.4
MODCARGO_CRATES +=	backtrace	0.3.30
MODCARGO_CRATES +=	backtrace-sys	0.1.28
MODCARGO_CRATES +=	bitflags	1.1.0
MODCARGO_CRATES +=	blake2-rfc	0.2.18
MODCARGO_CRATES +=	block-buffer	0.7.3
MODCARGO_CRATES +=	block-padding	0.1.4
MODCARGO_CRATES +=	bstr	0.1.4
MODCARGO_CRATES +=	byte-tools	0.3.1
MODCARGO_CRATES +=	bytecount	0.5.1
MODCARGO_CRATES +=	byteorder	1.3.2
MODCARGO_CRATES +=	cc	1.0.37
MODCARGO_CRATES +=	cfg-if	0.1.9
MODCARGO_CRATES +=	clap	2.33.0
MODCARGO_CRATES +=	cloudabi	0.0.3
MODCARGO_CRATES +=	constant_time_eq	0.1.3
MODCARGO_CRATES +=	crossbeam-channel	0.3.8
MODCARGO_CRATES +=	crossbeam-deque	0.2.0
MODCARGO_CRATES +=	crossbeam-epoch	0.3.1
MODCARGO_CRATES +=	crossbeam-utils	0.2.2
MODCARGO_CRATES +=	crossbeam-utils	0.6.5
MODCARGO_CRATES +=	digest	0.8.0
MODCARGO_CRATES +=	dirs	2.0.1
MODCARGO_CRATES +=	dirs-sys	0.3.3
MODCARGO_CRATES +=	dtoa	0.4.4
MODCARGO_CRATES +=	either	1.5.2
MODCARGO_CRATES +=	encoding_rs	0.8.17
MODCARGO_CRATES +=	encoding_rs_io	0.1.6
MODCARGO_CRATES +=	env_logger	0.6.1
MODCARGO_CRATES +=	failure	0.1.5
MODCARGO_CRATES +=	failure_derive	0.1.5
MODCARGO_CRATES +=	fake-simd	0.1.2
MODCARGO_CRATES +=	fnv	1.0.6
MODCARGO_CRATES +=	fuchsia-cprng	0.1.1
MODCARGO_CRATES +=	generic-array	0.12.0
MODCARGO_CRATES +=	git2	0.9.1
MODCARGO_CRATES +=	globset	0.4.3
MODCARGO_CRATES +=	grep-matcher	0.1.2
MODCARGO_CRATES +=	grep-searcher	0.1.4
MODCARGO_CRATES +=	half	1.3.0
MODCARGO_CRATES +=	handlebars	1.1.0
MODCARGO_CRATES +=	hex	0.3.2
MODCARGO_CRATES +=	humantime	1.2.0
MODCARGO_CRATES +=	idna	0.1.5
MODCARGO_CRATES +=	ignore	0.4.7
MODCARGO_CRATES +=	itoa	0.4.4
MODCARGO_CRATES +=	kernel32-sys	0.2.2
MODCARGO_CRATES +=	lazy_static	1.3.0
MODCARGO_CRATES +=	libc	0.2.58
MODCARGO_CRATES +=	libgit2-sys	0.8.0
MODCARGO_CRATES +=	libz-sys	1.0.25
MODCARGO_CRATES +=	linked-hash-map	0.5.2
MODCARGO_CRATES +=	log	0.4.6
MODCARGO_CRATES +=	maplit	1.0.1
MODCARGO_CRATES +=	matches	0.1.8
MODCARGO_CRATES +=	memchr	2.2.0
MODCARGO_CRATES +=	memmap	0.7.0
MODCARGO_CRATES +=	memoffset	0.2.1
MODCARGO_CRATES +=	nodrop	0.1.13
MODCARGO_CRATES +=	num_cpus	1.10.1
MODCARGO_CRATES +=	numtoa	0.1.0
MODCARGO_CRATES +=	opaque-debug	0.2.2
MODCARGO_CRATES +=	percent-encoding	1.0.1
MODCARGO_CRATES +=	pest	2.1.1
MODCARGO_CRATES +=	pest_derive	2.1.0
MODCARGO_CRATES +=	pest_generator	2.1.0
MODCARGO_CRATES +=	pest_meta	2.1.1
MODCARGO_CRATES +=	pkg-config	0.3.14
MODCARGO_CRATES +=	proc-macro2	0.4.30
MODCARGO_CRATES +=	quick-error	1.2.2
MODCARGO_CRATES +=	quote	0.6.12
MODCARGO_CRATES +=	rand	0.6.5
MODCARGO_CRATES +=	rand_chacha	0.1.1
MODCARGO_CRATES +=	rand_core	0.3.1
MODCARGO_CRATES +=	rand_core	0.4.0
MODCARGO_CRATES +=	rand_hc	0.1.0
MODCARGO_CRATES +=	rand_isaac	0.1.1
MODCARGO_CRATES +=	rand_jitter	0.1.4
MODCARGO_CRATES +=	rand_os	0.1.3
MODCARGO_CRATES +=	rand_pcg	0.1.2
MODCARGO_CRATES +=	rand_xorshift	0.1.1
MODCARGO_CRATES +=	rayon	1.0.3
MODCARGO_CRATES +=	rayon-core	1.4.1
MODCARGO_CRATES +=	rdrand	0.4.0
MODCARGO_CRATES +=	redox_syscall	0.1.54
MODCARGO_CRATES +=	redox_termios	0.1.1
MODCARGO_CRATES +=	redox_users	0.3.0
MODCARGO_CRATES +=	regex	1.1.7
MODCARGO_CRATES +=	regex-syntax	0.6.7
MODCARGO_CRATES +=	remove_dir_all	0.5.1
MODCARGO_CRATES +=	rustc-demangle	0.1.15
MODCARGO_CRATES +=	ryu	0.2.8
MODCARGO_CRATES +=	same-file	1.0.4
MODCARGO_CRATES +=	scoped_threadpool	0.1.9
MODCARGO_CRATES +=	scopeguard	0.3.3
MODCARGO_CRATES +=	serde	1.0.92
MODCARGO_CRATES +=	serde_cbor	0.9.0
MODCARGO_CRATES +=	serde_derive	1.0.92
MODCARGO_CRATES +=	serde_json	1.0.39
MODCARGO_CRATES +=	serde_yaml	0.8.9
MODCARGO_CRATES +=	sha-1	0.8.1
MODCARGO_CRATES +=	smallvec	0.6.10
MODCARGO_CRATES +=	strsim	0.8.0
MODCARGO_CRATES +=	syn	0.15.35
MODCARGO_CRATES +=	synstructure	0.10.2
MODCARGO_CRATES +=	tempfile	3.0.8
MODCARGO_CRATES +=	term_size	0.3.1
MODCARGO_CRATES +=	termcolor	1.0.5
MODCARGO_CRATES +=	termion	1.5.2
MODCARGO_CRATES +=	textwrap	0.11.0
MODCARGO_CRATES +=	thread_local	0.3.6
MODCARGO_CRATES +=	toml	0.5.1
MODCARGO_CRATES +=	typenum	1.10.0
MODCARGO_CRATES +=	ucd-trie	0.1.1
MODCARGO_CRATES +=	ucd-util	0.1.3
MODCARGO_CRATES +=	unicode-bidi	0.3.4
MODCARGO_CRATES +=	unicode-normalization	0.1.8
MODCARGO_CRATES +=	unicode-width	0.1.5
MODCARGO_CRATES +=	unicode-xid	0.1.0
MODCARGO_CRATES +=	url	1.7.2
MODCARGO_CRATES +=	utf8-ranges	1.0.3
MODCARGO_CRATES +=	vcpkg	0.2.6
MODCARGO_CRATES +=	vec_map	0.8.1
MODCARGO_CRATES +=	walkdir	2.2.8
MODCARGO_CRATES +=	winapi	0.2.8
MODCARGO_CRATES +=	winapi	0.3.7
MODCARGO_CRATES +=	winapi-build	0.1.1
MODCARGO_CRATES +=	winapi-i686-pc-windows-gnu	0.4.0
MODCARGO_CRATES +=	winapi-util	0.1.2
MODCARGO_CRATES +=	winapi-x86_64-pc-windows-gnu	0.4.0
MODCARGO_CRATES +=	wincolor	1.0.1
MODCARGO_CRATES +=	yaml-rust	0.4.3

#USE_GMAKE =		Yes
#USE_GROFF =		Yes
# Programs that require GNU libtool to build instead of the OpenBSD one
# should use this option. Add a comment explaining why. Don't use this if
# a port requires libtool's .m4 files but otherwise can use OpenBSD libtool,
# in that case use "BUILD_DEPENDS=devel/libtool" instead.
#USE_LIBTOOL=		gnu
# Set CONFIGURE_STYLE to value corresponding to some standard configuration
#	  perl [modbuild]: perl's MakeMaker Makefile.PL (modbuild: perl's
#	  Module::Build Build.PL)
#	  gnu [autoconf] [old] [dest]: gnu style configure (old: no
#	  sysconfdir), (dest: add DESTDIR, does not handle it),
#	  autoconf: run autoconf to regenerate configure script. implies gnu.
#	            (see also "do-gen" target below).
#	XXX: cygnus products do NOT use autoconf for making the main
#		configure from configure.in
#	  imake [noman]: port uses imake for configuration.
#	  (noman: no man page installation)
#	  simple: port has its own configure script
#	  none: override default CONFIGURE_STYLE coming from a module
#	        (needed for some ports using lang/python, etc.)
#CONFIGURE_STYLE =	
#CONFIGURE_SCRIPT =	??? (if other than configure)
#CONFIGURE_ARGS =	???
#CONFIGURE_ENV =	???

# for gnu stuff
#AUTOCONF_VERSION =	??? (defaults to 2.13)
#AUTOMAKE_VERSION =	??? (defaults to 1.4)
# config.guess and others are copied here
#MODGNU_CONFIG_GUESS_DIRS = ??? (defaults to ${WRKSRC})

# Is the build automagic or is it interactive
#
#IS_INTERACTIVE =		Yes
#TEST_IS_INTERACTIVE =		Yes

# Assume you have one multiple choice flavor: 1 2 3 and switches a b.
# You would write
#
#FLAVORS =	1 2 3 a b
#FLAVOR ?=
# grab multiple choice value
#CHOICE = ${FLAVOR:Na:Nb}
# check that CHOICE is 1 OR 2 OR 3, or error out
#.if ${CHOICE} == "1"
# code for 1
#.elif ${CHOICE} == "2"
# code for 2
#.elif ${CHOICE} == "3"
# code for 3
#.else
#ERRORS += "Fatal: Conflicting flavor: ${FLAVOR}"
#.endif
# check for switches
#.if ${FLAVOR:Ma}
# code for a
#.endif
#.if ${FLAVOR:Mb}
# code for b
#.endif

# Things that we don't want to do for this port/package
# Generally, DON'T set anything to No if it's not needed.
# The time gained is not worth it.
#
#NO_BUILD =		Yes
#NO_TEST =		Yes

# Overrides for default values
#
#CFLAGS =		???
#LDFLAGS =		???
#MAKE_FILE =		???
#PKG_ARCH =		??? (* for arch-independent packages)
#WRKDIST =		??? if other than ${WRKDIR}/${DISTNAME}
#WRKSRC =		??? if other than ${WRKDIST}
#WRKBUILD =		??? if other than ${WRKSRC}
#WRKCONF =		??? if other than ${WRKBUILD}

#ALL_TARGET =		???
#INSTALL_TARGET =	???
#TEST_TARGET =		???

# For ports that use a script or autoreconf to generate autoconf/automake
# files (where "CONFIGURE_STYLE=autoconf" isn't enough), use some/all of these
# dependencies, and add a do-gen target:
# 
#BUILD_DEPENDS =	${MODGNU_AUTOCONF_DEPENDS} \
#			${MODGNU_AUTOMAKE_DEPENDS} \
#			devel/libtool
#
#do-gen:
#	cd ${WRKSRC}; ${AUTOCONF_ENV} ./autogen.sh

.include <bsd.port.mk>

# $FreeBSD: src/lib/libbegemot/Makefile,v 1.5.2.1.6.1 2010/12/21 17:09:25 kensmith Exp $

LIBBEGEMOT_DIR=${.CURDIR}/../../contrib/libbegemot

.PATH: ${LIBBEGEMOT_DIR}

LIB=	begemot
SHLIB_MAJOR= 4
SHLIBDIR?= /lib

# WARNS?=	6

CFLAGS+=	-DUSE_SELECT -DQUADFMT='"ll"'
SRCS=	rpoll.c
INCS=	rpoll.h
MAN=	rpoll.3

CLEANFILES= rpoll.3
rpoll.3: rpoll.man
	cat ${.ALLSRC} > ${.TARGET}

MLINKS=	rpoll.3 poll_register.3		\
	rpoll.3 poll_unregister.3	\
	rpoll.3 poll_start_timer.3	\
	rpoll.3 poll_stop_timer.3	\
	rpoll.3 poll_dispatch.3

.include <bsd.lib.mk>

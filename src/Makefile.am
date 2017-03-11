include_HEADERS = ilclient.h
lib_LTLIBRARIES = libilclient.la

ILCLIENT_VERSION=1:0:0
libilclient_la_SOURCES = ilclient.c ilcore.c
libilclient_la_CPPFLAGS = \
	-DSTANDALONE \
	-D__STDC_CONSTANT_MACROS \
	-D__STDC_LIMIT_MACROS \
	-DTARGET_POSIX \
	-D_LINUX \
 -fPIC \
	-DPIC \
	-D_REENTRANT \
	-D_LARGEFILE64_SOURCE \
	-D_FILE_OFFSET_BITS=64 \
	-U_FORTIFY_SOURCE \
-Wall -g \
	-DHAVE_LIBOPENMAX=2 \
	-DOMX -DOMX_SKIP64BIT \
-ftree-vectorize -pipe \
	-DUSE_EXTERNAL_OMX \
	-DHAVE_LIBBCM_HOST \
	-DUSE_EXTERNAL_LIBBCM_HOST \
	-DUSE_VCHIQ_ARM \
-Wno-psabi \
	-I/opt/vc/include \
	-I/opt/vc/include/interface/vcos/pthreads \
	-I/opt/vc/include/interface/vmcs_host/linux

libilclient_la_LDFLAGS = \
	-version-info $(ILCLIENT_VERSION) \
	-Wl,--no-undefined \
	-L/opt/vc/lib

libilclient_la_LIBADD = \
	-lvcos \
	-lopenmaxil \
	-lbcm_host \
	-lpthread

unused=	-lGLESv2 \
	-lEGL \
	-lvchiq_arm \
	-lrt \
	-lm

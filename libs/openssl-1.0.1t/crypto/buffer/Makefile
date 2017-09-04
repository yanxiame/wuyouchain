#
# OpenSSL/crypto/buffer/Makefile
#

DIR=	buffer
TOP=	../..
CC=	cc
INCLUDES= -I.. -I$(TOP) -I../../include
CFLAG=-g
MAKEFILE=	Makefile
AR=		ar r

CFLAGS= $(INCLUDES) $(CFLAG)

GENERAL=Makefile
TEST=
APPS=

LIB=$(TOP)/libcrypto.a
LIBSRC= buffer.c buf_str.c buf_err.c
LIBOBJ= buffer.o buf_str.o buf_err.o

SRC= $(LIBSRC)

EXHEADER= buffer.h
HEADER=	$(EXHEADER)

ALL=    $(GENERAL) $(SRC) $(HEADER)

top:
	(cd ../..; $(MAKE) DIRS=crypto SDIRS=$(DIR) sub_all)

all:	lib

lib:	$(LIBOBJ)
	$(AR) $(LIB) $(LIBOBJ)
	$(RANLIB) $(LIB) || echo Never mind.
	@touch lib

files:
	$(PERL) $(TOP)/util/files.pl Makefile >> $(TOP)/MINFO

links:
	@$(PERL) $(TOP)/util/mklink.pl ../../include/openssl $(EXHEADER)
	@$(PERL) $(TOP)/util/mklink.pl ../../test $(TEST)
	@$(PERL) $(TOP)/util/mklink.pl ../../apps $(APPS)

install:
	@[ -n "$(INSTALLTOP)" ] # should be set by top Makefile...
	@headerlist="$(EXHEADER)"; for i in $$headerlist ; \
	do  \
	(cp $$i $(INSTALL_PREFIX)$(INSTALLTOP)/include/openssl/$$i; \
	chmod 644 $(INSTALL_PREFIX)$(INSTALLTOP)/include/openssl/$$i ); \
	done;

tags:
	ctags $(SRC)

tests:

lint:
	lint -DLINT $(INCLUDES) $(SRC)>fluff

update: depend

depend:
	@[ -n "$(MAKEDEPEND)" ] # should be set by upper Makefile...
	$(MAKEDEPEND) -- $(CFLAG) $(INCLUDES) $(DEPFLAG) -- $(PROGS) $(LIBSRC)

dclean:
	$(PERL) -pe 'if (/^# DO NOT DELETE THIS LINE/) {print; exit(0);}' $(MAKEFILE) >Makefile.new
	mv -f Makefile.new $(MAKEFILE)

clean:
	rm -f *.o *.obj lib tags core .pure .nfs* *.old *.bak fluff

# DO NOT DELETE THIS LINE -- make depend depends on it.

buf_err.o: ../../include/openssl/bio.h ../../include/openssl/buffer.h
buf_err.o: ../../include/openssl/crypto.h ../../include/openssl/e_os2.h
buf_err.o: ../../include/openssl/err.h ../../include/openssl/lhash.h
buf_err.o: ../../include/openssl/opensslconf.h ../../include/openssl/opensslv.h
buf_err.o: ../../include/openssl/ossl_typ.h ../../include/openssl/safestack.h
buf_err.o: ../../include/openssl/stack.h ../../include/openssl/symhacks.h
buf_err.o: buf_err.c
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
buf_err.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
buf_str.o: ../../e_os.h ../../include/openssl/bio.h
buf_str.o: ../../include/openssl/buffer.h ../../include/openssl/crypto.h
buf_str.o: ../../include/openssl/e_os2.h ../../include/openssl/err.h
buf_str.o: ../../include/openssl/lhash.h ../../include/openssl/opensslconf.h
buf_str.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
buf_str.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
buf_str.o: ../../include/openssl/symhacks.h ../cryptlib.h buf_str.c
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
buf_str.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
buffer.o: ../../e_os.h ../../include/openssl/bio.h
buffer.o: ../../include/openssl/buffer.h ../../include/openssl/crypto.h
buffer.o: ../../include/openssl/e_os2.h ../../include/openssl/err.h
buffer.o: ../../include/openssl/lhash.h ../../include/openssl/opensslconf.h
buffer.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
buffer.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
buffer.o: ../../include/openssl/symhacks.h ../cryptlib.h buffer.c
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
buffer.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h

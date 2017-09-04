#
# OpenSSL/crypto/lhash/Makefile
#

DIR=	lhash
TOP=	../..
CC=	cc
INCLUDES=
CFLAG=-g
MAKEFILE=	Makefile
AR=		ar r

CFLAGS= $(INCLUDES) $(CFLAG)

GENERAL=Makefile
TEST=
APPS=

LIB=$(TOP)/libcrypto.a
LIBSRC=lhash.c lh_stats.c
LIBOBJ=lhash.o lh_stats.o

SRC= $(LIBSRC)

EXHEADER= lhash.h
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

lh_stats.o: ../../e_os.h ../../include/openssl/bio.h
lh_stats.o: ../../include/openssl/buffer.h ../../include/openssl/crypto.h
lh_stats.o: ../../include/openssl/e_os2.h ../../include/openssl/err.h
lh_stats.o: ../../include/openssl/lhash.h ../../include/openssl/opensslconf.h
lh_stats.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
lh_stats.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
lh_stats.o: ../../include/openssl/symhacks.h ../cryptlib.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
lh_stats.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
lh_stats.o: lh_stats.c
lhash.o: ../../include/openssl/bio.h ../../include/openssl/crypto.h
lhash.o: ../../include/openssl/e_os2.h ../../include/openssl/lhash.h
lhash.o: ../../include/openssl/opensslconf.h ../../include/openssl/opensslv.h
lhash.o: ../../include/openssl/ossl_typ.h ../../include/openssl/safestack.h
lhash.o: ../../include/openssl/stack.h ../../include/openssl/symhacks.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
lhash.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
lhash.o: lhash.c

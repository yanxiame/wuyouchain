#
# OpenSSL/crypto/stack/Makefile
#

DIR=	stack
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
LIBSRC=stack.c
LIBOBJ=stack.o

SRC= $(LIBSRC)

EXHEADER= stack.h safestack.h
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

stack.o: ../../e_os.h ../../include/openssl/asn1.h ../../include/openssl/bio.h
stack.o: ../../include/openssl/buffer.h ../../include/openssl/crypto.h
stack.o: ../../include/openssl/e_os2.h ../../include/openssl/err.h
stack.o: ../../include/openssl/lhash.h ../../include/openssl/obj_mac.h
stack.o: ../../include/openssl/objects.h ../../include/openssl/opensslconf.h
stack.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
stack.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
stack.o: ../../include/openssl/symhacks.h ../cryptlib.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pthread_time.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/sys/timeb_s.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/timeb.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/time.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
stack.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
stack.o: stack.c

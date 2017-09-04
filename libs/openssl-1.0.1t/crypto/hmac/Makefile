#
# OpenSSL/crypto/md/Makefile
#

DIR=	hmac
TOP=	../..
CC=	cc
INCLUDES=
CFLAG=-g
MAKEFILE=	Makefile
AR=		ar r

CFLAGS= $(INCLUDES) $(CFLAG)

GENERAL=Makefile
TEST=hmactest.c
APPS=

LIB=$(TOP)/libcrypto.a
LIBSRC=hmac.c hm_ameth.c hm_pmeth.c
LIBOBJ=hmac.o hm_ameth.o hm_pmeth.o

SRC= $(LIBSRC)

EXHEADER= hmac.h
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

hm_ameth.o: ../../e_os.h ../../include/openssl/asn1.h
hm_ameth.o: ../../include/openssl/bio.h ../../include/openssl/buffer.h
hm_ameth.o: ../../include/openssl/crypto.h ../../include/openssl/e_os2.h
hm_ameth.o: ../../include/openssl/err.h ../../include/openssl/evp.h
hm_ameth.o: ../../include/openssl/lhash.h ../../include/openssl/obj_mac.h
hm_ameth.o: ../../include/openssl/objects.h ../../include/openssl/opensslconf.h
hm_ameth.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
hm_ameth.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
hm_ameth.o: ../../include/openssl/symhacks.h ../asn1/asn1_locl.h ../cryptlib.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pthread_time.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/sys/timeb_s.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/timeb.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/time.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
hm_ameth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
hm_ameth.o: hm_ameth.c
hm_pmeth.o: ../../e_os.h ../../include/openssl/asn1.h
hm_pmeth.o: ../../include/openssl/bio.h ../../include/openssl/buffer.h
hm_pmeth.o: ../../include/openssl/conf.h ../../include/openssl/crypto.h
hm_pmeth.o: ../../include/openssl/e_os2.h ../../include/openssl/ec.h
hm_pmeth.o: ../../include/openssl/ecdh.h ../../include/openssl/ecdsa.h
hm_pmeth.o: ../../include/openssl/err.h ../../include/openssl/evp.h
hm_pmeth.o: ../../include/openssl/hmac.h ../../include/openssl/lhash.h
hm_pmeth.o: ../../include/openssl/obj_mac.h ../../include/openssl/objects.h
hm_pmeth.o: ../../include/openssl/opensslconf.h
hm_pmeth.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
hm_pmeth.o: ../../include/openssl/pkcs7.h ../../include/openssl/safestack.h
hm_pmeth.o: ../../include/openssl/sha.h ../../include/openssl/stack.h
hm_pmeth.o: ../../include/openssl/symhacks.h ../../include/openssl/x509.h
hm_pmeth.o: ../../include/openssl/x509_vfy.h ../../include/openssl/x509v3.h
hm_pmeth.o: ../cryptlib.h ../evp/evp_locl.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pthread_time.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/sys/timeb_s.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/timeb.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/time.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
hm_pmeth.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
hm_pmeth.o: hm_pmeth.c
hmac.o: ../../e_os.h ../../include/openssl/asn1.h ../../include/openssl/bio.h
hmac.o: ../../include/openssl/buffer.h ../../include/openssl/crypto.h
hmac.o: ../../include/openssl/e_os2.h ../../include/openssl/err.h
hmac.o: ../../include/openssl/evp.h ../../include/openssl/hmac.h
hmac.o: ../../include/openssl/lhash.h ../../include/openssl/obj_mac.h
hmac.o: ../../include/openssl/objects.h ../../include/openssl/opensslconf.h
hmac.o: ../../include/openssl/opensslv.h ../../include/openssl/ossl_typ.h
hmac.o: ../../include/openssl/safestack.h ../../include/openssl/stack.h
hmac.o: ../../include/openssl/symhacks.h ../cryptlib.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_bsd_types.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_mac.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_off_t.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_pop.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_print_push.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_secapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_stdarg.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_mingw_unicode.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/_timeval.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/apisetcconv.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/basetsd.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/bemapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/crtdefs.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ctype.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/datetimeapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/debugapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errhandlingapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/errno.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/excpt.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fcntl.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fibersapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fileapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/fltwinerror.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/guiddef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/handleapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/heapapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/imm.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/in6addr.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/inaddr.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/interlockedapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/io.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ioapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/jobapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ktmtypes.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/libloaderapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/limits.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/malloc.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mcx.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/memoryapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwinbase.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/minwindef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/mstcpip.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namedpipeapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/namespaceapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/poppack.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processenv.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processthreadsapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/processtopologyapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/profileapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_fd_types.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_mreq1.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ip_types.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_socket_types.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_ws1_undef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsa_errnos.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/_wsadata.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/psdk_inc/intrin-impl.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack1.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack2.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack4.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pshpack8.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/pthread_time.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/qos.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/realtimeapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/reason.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sal.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdkddkver.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_ddk.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sdks/_mingw_directx.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdio_s.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stdlib_s.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/stralign_s.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/string_s.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sec_api/sys/timeb_s.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securityappcontainer.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/securitybaseapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/specstrings.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdarg.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stddef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdio.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stdlib.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stralign.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/string.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/stringapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/swprintf.inl
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/synchapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/timeb.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sys/types.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/sysinfoapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/systemtopologyapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoolapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/threadpoollegacyapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/time.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/timezoneapi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/tvout.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/utilapiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/vadefs.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/virtdisk.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winapifamily.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winbase.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wincon.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/windows.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winerror.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wingdi.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnetwk.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnls.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winnt.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winreg.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsock2.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winsvc.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winuser.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/winver.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wnnc.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/wow64apiset.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2def.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2ipdef.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/i686-w64-mingw32/include/ws2tcpip.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/limits.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include-fixed/syslimits.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stdarg.h
hmac.o: c:/Qt/Qt5.7.0/Tools/mingw530_32/lib/gcc/i686-w64-mingw32/5.3.0/include/stddef.h
hmac.o: hmac.c

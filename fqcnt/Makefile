CFLAGS=-g -Wall -O2
LIBS=-lz
PROG=fqcnt_c1_kseq fqcnt_nim1_klib
NIM=nim

.PHONY:all clean

all:$(PROG)

fqcnt_c1_kseq:fqcnt_c1_kseq.c ../lib/kseq.h
	$(CC) $(CFLAGS) -I../lib -o $@ $< $(LIBS)

fqcnt_nim1_klib:fqcnt_nim1_klib.nim ../lib/klib.nim
	$(NIM) c -d:release -d:nimEmulateOverflowChecks -p:../lib -o:$@ $<

clean:
	rm -fr *.dSYM $(PROG)

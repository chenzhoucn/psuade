
# The following system parameters are for a Linux host.
# ARCH   = LINUX

CC     = gcc -g -Wall
CXX    = g++ -g -Wall
F77    = f77 
AR     = ar
RANLIB = true

OBJS = construct.o akconst.o primes.o gfields.o galois.o memory.o \
       boselink.o  oa.o

.c.o:
	@$(CC) $(CFLAGS) -w -g -c $<

./libbose.a: $(OBJS)
	$(AR) ruv $@ $(OBJS)
	$(RANLIB) $@

clean:
	@rm -f *.o ./libbose.a

realclean:
	rm -f *.o ; rm -f ./libbose.a

construct.o: construct.c galois.h
akconst.o: akconst.c galois.h
primes.o: primes.c
gfields.o: gfields.c galois.h xtnset.h xtndeclare.h xtndispatch.h
galois.o: galois.c galois.h
memory.o: memory.c
boselink.o: boselink.c
oa.o: oa.c


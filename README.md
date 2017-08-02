# issues
# -Werror in Docker:
root@82853d8df2a5:/scratch/src# ./Build snap
--2017-08-01 21:31:29--  http://topaz.genetics.utah.edu/maker_downloads/static/locations
Resolving topaz.genetics.utah.edu (topaz.genetics.utah.edu)... 155.101.145.49
Connecting to topaz.genetics.utah.edu (topaz.genetics.utah.edu)|155.101.145.49|:80... connected.
HTTP request sent, awaiting response... 416 Requested Range Not Satisfiable

    The file is already fully retrieved; nothing to do.

Downloading snap...
--2017-08-01 21:31:30--  http://korflab.ucdavis.edu/Software/snap-2013-11-29.tar.gz
Resolving korflab.ucdavis.edu (korflab.ucdavis.edu)... 128.120.143.145
Connecting to korflab.ucdavis.edu (korflab.ucdavis.edu)|128.120.143.145|:80... connected.
HTTP request sent, awaiting response... 416 Requested Range Not Satisfiable

    The file is already fully retrieved; nothing to do.

Unpacking snap tarball...
Configuring snap...
make gcc
make[1]: Entering directory '/scratch/exe/snap'
cd Zoe; make;
make[2]: Entering directory '/scratch/exe/snap/Zoe'
make gcc
make[3]: Entering directory '/scratch/exe/snap/Zoe'
make zoe-loop  CC="gcc" CFLAGS="-O2 -Wall -Werror"
make[4]: Entering directory '/scratch/exe/snap/Zoe'
gcc -O2 -Wall -Werror -c -o zoe-loop.o zoe-loop.c
gcc -O2 -Wall -Werror -c -o zoeAlignment.o zoeAlignment.c
zoeAlignment.c: In function 'zoeHSPCmpQuery':
zoeAlignment.c:678:50: error: self-comparison always evaluates to false [-Werror=tautological-compare]
  else if (h1->q_start > h2->q_start && h2->q_end > h2->q_end) return  1;
                                                  ^
zoeAlignment.c: In function 'zoeHSPCmpSbjct':
zoeAlignment.c:684:50: error: self-comparison always evaluates to false [-Werror=tautological-compare]
  else if (h1->s_start > h2->s_start && h2->s_end > h2->s_end) return  1;
                                                  ^
cc1: all warnings being treated as errors
Makefile:110: recipe for target 'zoeAlignment.o' failed
make[4]: *** [zoeAlignment.o] Error 1
make[4]: Leaving directory '/scratch/exe/snap/Zoe'
Makefile:95: recipe for target 'gcc' failed
make[3]: *** [gcc] Error 2
make[3]: Leaving directory '/scratch/exe/snap/Zoe'
Makefile:58: recipe for target 'default' failed
make[2]: *** [default] Error 2
make[2]: Leaving directory '/scratch/exe/snap/Zoe'
Makefile:96: recipe for target 'gcc' failed
make[1]: *** [gcc] Error 2
make[1]: Leaving directory '/scratch/exe/snap'
Makefile:58: recipe for target 'default' failed
make: *** [default] Error 2


ERROR: Failed installing snap, now cleaning installation path...
You may need to install snap manually.




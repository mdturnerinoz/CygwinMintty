CYGWIN - mintty correct $HOME and allows SSH with 

This is the default CGYWIN mintty definition:

D:\cygwin\bin\mintty.exe -i /Cygwin-Terminal.ico -

THAT one does NOT allow the correct $HOME (i.e. it defaults to the
WIN7 home (e.g. /cygdrive/c/Users/marty) INSTEAD of /home/marty.

ALSO, the CORRECT bash location is /usr/bin/bash and NOT /bin/bash
where cygwin tries to define it; THE following works for BOTH 
scenarios:

D:\cygwin\bin\mintty.exe -i /Cygwin-Terminal.ico /bin/env HOME=/home/marty /usr/bin/bash -l 
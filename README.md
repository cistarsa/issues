```bash
# issues
# -Werror in Docker:
# error when running the Maker executable 
STATUS: Parsing control files...
WARNING: RepBase is not installed for RepeatMasker.
# led me to attempt to download RepBase via the ./Build repeatmasker command in the Maker/src directory:
Connecting to www.repeatmasker.org (www.repeatmasker.org)|174.127.185.155|:80... connected.
HTTP request sent, awaiting response... 416 Requested Range Not Satisfiable

    The file is already fully retrieved; nothing to do.

Unpacking RepeatMasker tarball...

If are a registered user of RepBase, then MAKER can
download and install RepBase for RepeatMasker for you.
Do you want to do this? [Y ]Y

* NOTE: Register at http://www.girinst.org/

Please enter your username: [ ]kingcohn1
Please enter your Password: [ ]ephsdl
Downloading RepBase...
--2017-08-03 21:06:38--  http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/repeatmaskerlibraries-20140131.tar.gz
Resolving www.girinst.org (www.girinst.org)... 52.9.119.183
Connecting to www.girinst.org (www.girinst.org)|52.9.119.183|:80... connected.
HTTP request sent, awaiting response... 401 Authorization Required
Authentication selected: Basic realm="Repbase"
Connecting to www.girinst.org (www.girinst.org)|52.9.119.183|:80... connected.
HTTP request sent, awaiting response... 404 Not Found
2017-08-03 21:06:38 ERROR 404: Not Found.

Download failed: http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/repeatmaskerlibraries-20140131.tar.gz
Alternate version or url available: http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/repeatmaskerlibraries-20150807.tar.gz
Do want to try the alternate version/url? [Y ]y
--2017-08-03 21:06:48--  http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/repeatmaskerlibraries-20150807.tar.gz
Resolving www.girinst.org (www.girinst.org)... 52.9.119.183
Connecting to www.girinst.org (www.girinst.org)|52.9.119.183|:80... connected.
HTTP request sent, awaiting response... 401 Authorization Required
Authentication selected: Basic realm="Repbase"
Connecting to www.girinst.org (www.girinst.org)|52.9.119.183|:80... connected.
HTTP request sent, awaiting response... 404 Not Found
2017-08-03 21:06:48 ERROR 404: Not Found.



ERROR: Failed installing RepBase, now cleaning installation path...
You may need to install RepBase manually.

# this hyperlink has expired and the new library is found at http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/RepBaseRepeatMaskerEdition-20170127.tar.gz, but I can't seem to download this from the docker environment as I'm not able to authenticate. 

root@82853d8df2a5:/scratch/src# wget http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/RepBaseRepeatMaskerEdition-20170127.tar.gz
--2017-08-03 21:55:22--  http://www.girinst.org/server/RepBase/protected/repeatmaskerlibraries/RepBaseRepeatMaskerEdition-20170127.tar.gz
Resolving www.girinst.org (www.girinst.org)... 52.9.119.183
Connecting to www.girinst.org (www.girinst.org)|52.9.119.183|:80... connected.
HTTP request sent, awaiting response... 401 Authorization Required

Username/Password Authentication Failed.

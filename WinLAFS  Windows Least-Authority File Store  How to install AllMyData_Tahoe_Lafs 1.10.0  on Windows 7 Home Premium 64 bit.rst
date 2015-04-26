                    **WinLAFS:**

**Windows Least-Authority File Store**

**How to install AllMyData\_Tahoe\_Lafs 1.10.0**

**on Windows 7 Home Premium 64 bit**

[i installed already WinLAFS on 7win32 see WinLAFS:How to install AllMyData\_Tahoe\_Lafs 1.10.0 on Windows 7 bit 32 ; it should be possible to install python for 32bit windows and 32bit dependencies on win7bit64 ]

[but i gave 64bit a try]

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

If you are attracted by errors, failures and user warnings on this Site,

but only like to install allmydata-tahoe-1.10.0 then start with 0 (zero):

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

0: Successful install may fail if you used already python:

0a: uninstalled all installed dependencies related to python

0b: uninstalled python

0c: delete the python directory

0d: delete the AllMyData\_Tahoe\_Lafs directory

0e: start from scratch at A.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**installing tahoe-lafs on 7win64 with twisted 13**

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

preinstall:

python-2.7.9.

Twisted-13.0.0.

pywin32-217.

copy:

allmydata-tahoe-1.10.0

egenix\_pyopenssl-0.13.7-py2.7-win-amd64.egg

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

A. Unzip and Copy: allmydata-tahoe-1.10.0 to c:\\lafs (unzip and rename to "lafs" only)

from `https://tahoe-lafs.org/source/tahoe-lafs/releases/allmydata-tahoe-1.10.0.zip <https://tahoe-lafs.org/source/tahoe-lafs/releases/allmydata-tahoe-1.10.0.zip>`_

B. We don't follow: C:\\lafs\\docs\\quickstart.rst (open with word pad)

C. Install : python-2.7.9.amd64.msi at c:\\python27 ( check: set Add pyton.exe to Path

and advanced-> check: compile .py files to byte code after installation)

from `https://www.python.org/downloads/release/python-279/ <https://www.python.org/downloads/release/python-279/>`_

`https://www.python.org/ftp/python/2.7.9/python-2.7.9.amd64.msi <https://www.python.org/ftp/python/2.7.9/python-2.7.9.amd64.msi>`_

D. Install: Twisted-13.0.0.win-amd64-py2.7.msi

from `http://twistedmatrix.com/Releases/Twisted/13.0/ <http://twistedmatrix.com/Releases/Twisted/13.0/>`_

`http://twistedmatrix.com/Releases/Twisted/13.0/Twisted-13.0.0.win-amd64-py2.7.msi <http://twistedmatrix.com/Releases/Twisted/13.0/Twisted-13.0.0.win-amd64-py2.7.msi>`_

E. Install: pywin32-217.win-amd64-py2.7.exe

`http://sourceforge.net/projects/pywin32/files/pywin32/Build%20217/ <http://sourceforge.net/projects/pywin32/files/pywin32/Build%20217/>`_

`http://sourceforge.net/projects/pywin32/files/pywin32/Build%20217/pywin32-217.win-amd64-py2.7.exe/download <http://sourceforge.net/projects/pywin32/files/pywin32/Build%20217/pywin32-217.win-amd64-py2.7.exe/download>`_

F.Copy: egenix\_pyopenssl-0.13.7-py2.7-win-amd64.egg

and

Rename: to

c:\\tahoe-deps\\pyopenssl-0.13.7-py2.7-win-amd64.egg

from `https://www.egenix.com/products/python/pyOpenSSL/ <https://www.egenix.com/products/python/pyOpenSSL/>`_

[scroll down till:\ **Egg Distribution Installation** ]

`https://downloads.egenix.com/python/index/ucs2/egenix-pyopenssl/0.13.7/egenix\_pyopenssl-0.13.7-py2.7-win-amd64.egg <https://downloads.egenix.com/python/index/ucs2/egenix-pyopenssl/0.13.7/egenix_pyopenssl-0.13.7-py2.7-win-amd64.egg>`_

G.Run as administrator : C:\\lafs>\ **python setup.py build**

(Start menu/All Programs/Command Prompt/right click/\ **Run as administrator**/jes> cd c:\\lafs)

or like to read it all at : C:\\lafs\\setup\_build\_bin.txt

Run as administrator : C:\\lafs>\ **python setup.py build > setup\_build\_bin.txt**

(go drink a cup of coffee 3 min)

***1. Result: run thru ( it copying many somethings to -> build\\lib\\allmydata\\...\\...)***

H. Run as administrator : C:\\lafs>\ **bin\\tahoe --version**

***2.Result:***

***allmydata-tahoe: 1.10.0 [NL]foolscap: 0.7.0 [NL]pycryptopp: 0.6.0.1206569328141510525648634803928199668821045408958 [NL]fec: 1.4.22 [NL]Twisted: 13.0.0 [NL]Nevow: 0.11.1 [NL]zope.interface: unknown [NL]python: 2.7.9 [NL]platform: Windows-7-6.1.7601-SP1 [NL]***\ ***pyOpenSSL: 0.13.7***\ ***[NL]simplejson: 3.6.5 [NL]***\ ***pycrypto: 2.5***\ ***[NL]pyasn1: 0.1.7 [NL]mock: 1.0.1 [NL]setuptools: 0.6c16dev4 [NL]=NEW LINE***

i. Check: Test Grid is online

Tahoe Test Grid Status at `http://stats.pingdom.com/cvvac5t8l4fv/1300061 <http://stats.pingdom.com/cvvac5t8l4fv/1300061>`_

J.Run as administrator : C:\\lafs>\ **python setup.py trial**\ (self-tests)

if like to read all at C:\\lafs\\trial\_test\_result.txt

Run as administrator :C:\\lafs>**python setup.py trial > trial\_test\_result.txt**

(go drink a cup of coffee 19min)

***3. Result:***\ ***PASSED (skips=14, expectedFailures=3, successes=1117)***

This indicates you installed tahoe-lafs successful.

==================================================

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

If you are attracted by errors, failures and user warnings on this Site,

but only like to install allmydata-tahoe-1.10.0 then start with 0 (zero):

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

This following is about what happens if you follow the Install Advise at

C:\\lafs\\docs\\quickstart.rst (open with wordpad)

and this is the wrong , long, hard way along errors,failures and warnings.

----------------------------------------------------------------------------------------------

**Some Tahoe\_Lafs Installation Problems on windows 7 bit 64**

-------------------------------------------------------------------------------------------

[ because of my "success" installing tahoe-lafs at win7bit32,

i thought i am now a already skilled tahoe-lafs installer ]

I. Install: allmydata-tahoe-1.10.0 at c:\\lafs (unzip and rename to " lafs" only)

from `https://tahoe-lafs.org/source/tahoe-lafs/releases/allmydata-tahoe-1.10.0.zip <https://tahoe-lafs.org/source/tahoe-lafs/releases/allmydata-tahoe-1.10.0.zip>`_

II. allowances for "C:\\lafs" :

**As admin**\ selekt user "everybody" allow everything (all) for user "everybody"(all users)

start/computer/"C:\\"/Mouse right click at /"C:\\lafs"/properties/security

/edit/add/advanced/look for (users)/(select)/everybody (all)/OK/OK/

select user name /everybody (all)/\|V\|(check)/**allow**/all/and/allow/alter/OK

[this is a translation of the "path", look out for similar expressions if necessary]

[At this time i thought i solved a tmp-write problem,

but successful was only the RUN AS ADMINISTRATOR method ]

III. follow: C:\\lafs\\docs\\quickstart.rst (open with word pad)

IV. Install : python-2.7.9.msi at c:\\python27 ( check: set Add pyton.exe to Path and

advanced-> check: compile .py files to byte code after installation)

from `https://www.python.org/ftp/python/2.7.9/python-2.7.9.msi <https://www.python.org/ftp/python/2.7.9/python-2.7.9.msi>`_

V. Run: C:\\lafs>python setup.py build

(Start/Program files/command prompt > cd c:\\lafs)

or like to read it all at : C:\\lafs\\setup\_build\_bin.txt

Run: C:\\lafs>python setup.py build > setup\_build\_bin.txt

(go drink a cup of coffee)

***my 1.Result:***

**error: Installed distribution twisted 12.1.0 conflicts with requirement twisted>=13.0**

VI. Install: Twisted-13.0.0.win-amd64-py2.7.msi

from `http://twistedmatrix.com/Releases/Twisted/13.0/ <http://twistedmatrix.com/Releases/Twisted/13.0/>`_

`http://twistedmatrix.com/Releases/Twisted/13.0/Twisted-13.0.0.win-amd64-py2.7.msi <http://twistedmatrix.com/Releases/Twisted/13.0/Twisted-13.0.0.win-amd64-py2.7.msi>`_

VI. Delete: C:\\lafs

VII. Try again I.+II.+V. (install lafs + run lafs setup build bin)

***my 2. Result: error: Setup script exited with error: Unable to find vcvarsall.bat***

[reason: script like to compile and install cffi 0.9.2]

**[**\ Twisted-13.0.0 adds **tls - packages that are needed to work with TLS. =** service\_identity]

[dependencies of service\_identity:]

[------------------------------------------------------------------------------------------------------

`https://pypi.python.org/pypi/service\_identity <https://pypi.python.org/pypi/service_identity>`_

`https://pypi.python.org/packages/2.7/s/service\_identity/service\_identity-14.0.0-py2.py3-none-any.whl <https://pypi.python.org/packages/2.7/s/service_identity/service_identity-14.0.0-py2.py3-none-any.whl>`_

service-identity==14.0.0 requires pyopenssl>=0.12

`https://downloads.egenix.com/python/index/ucs2/egenix-pyopenssl/0.13.7/egenix\_pyopenssl-0.13.7-py2.7-win-amd64.egg <https://downloads.egenix.com/python/index/ucs2/egenix-pyopenssl/0.13.7/egenix_pyopenssl-0.13.7-py2.7-win-amd64.egg>`_

`https://www.egenix.com/cryptodownload/?file=egenix-pyopenssl-0.13.7.win-amd64-py2.7.msi <https://www.egenix.com/cryptodownload/?file=egenix-pyopenssl-0.13.7.win-amd64-py2.7.msi>`_

pyopenssl-0.13.7-py2.7-win-amd64.egg requires cryptography>=0.2.1 + (six>=1.5.2 )

`https://pypi.python.org/packages/cp27/c/cryptography/cryptography-0.4-cp27-none-win\_amd64.whl <https://pypi.python.org/packages/cp27/c/cryptography/cryptography-0.4-cp27-none-win_amd64.whl>`_

`https://pypi.python.org/packages/cp27/c/cryptography/cryptography-0.5-cp27-none-win\_amd64.whl <https://pypi.python.org/packages/cp27/c/cryptography/cryptography-0.5-cp27-none-win_amd64.whl>`_

cryptography-0.5-cp27-none-win\_amd64.whl requires cffi>=0.8

`http://www.lfd.uci.edu/~gohlke/pythonlibs/z94jfosk/cffi-0.9.2-cp27-none-win\_amd64.whl <http://www.lfd.uci.edu/~gohlke/pythonlibs/z94jfosk/cffi-0.9.2-cp27-none-win_amd64.whl>`_

cffi-0.9.2-cp27-none-win\_amd64.whl requires pycparser

---------------------------------------------------------------------------------------------------------------------------]

tabula rasa: 0a-0e

I.-IV. + VI.

copy egenix-pyopenssl-0.13.7-py2.7-win-amd64.egg to c\\tahoe-deps

copy cffi-0.9.2-cp27-none-win\_amd64.whl to c:\\lafs

copy cryptography-0.5-cp27-none-win\_amd64.whl to c:\\lafs

pip install cffi-0.9.2-cp27-none-win\_amd64.whl

pip install cryptography-0.5-cp27-none-win\_amd64.whl

install egenix-pyopenssl-0.13.7.win-amd64-py2.7.msi

run thru

install win32api= pywin32

FAILED (skips=14, expectedFailures=3, failures=1, errors=4, successes=1116) [1]

-------------------------------------------------------------------------------------------------------------------------

try install with egg only no msi (egenix-pyopenssl-0.13.7.win-amd64-py2.7 )

----------------------------------------------------------------------------------------------------

tabula rasa: 0a-0e

I.-IV. + VI.

preinstall:

pyton27

Twisted-13.0.0.win-amd64-py2.7.msi

win32api = pywin32

copy egenix-pyopenssl-0.13.7-py2.7-win-amd64.egg to c\\tahoe-deps

error: Setup script exited with error: Unable to find vcvarsall.bat

[need pip install off cffi ?] no -> rename

rename [!]+copy pyopenssl-0.13.7-py2.7-win-amd64.egg [!] to c\\tahoe-deps

FAILED (skips=14, expectedFailures=3, failures=1, errors=3, successes=1116)

[------------------------How to prevent the last failure ?---------------------------------------------------------

**[ and we know now any shell from an administrator account is not an administrator shell**

**[ this step is not necessary if you run as administrator:**

[ II. allowances for "C:\\lafs" :

**[ As admin**\ selekt user "everybody" allow everything (all) for user "everybody"(all users)

[ start/computer/"C:\\"/Mouse right click at /"C:\\lafs"/properties/security

[ /edit/add/advanced/look for (users)/(select)/everybody (all)/OK/OK/

[ select user name /everybody (all)/\|V\|(check)/**allow**/all/and/allow/alter/OK

[ [this is a translation of the "path", look out for similar expressions if necessary]

**[ it helps partly to shrink the failures to only one, but you still get a fail**

------------------------------------------------------------------------------------------------------------]

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

If you are attracted by errors, failures and user warnings on this Site,

but only like to install allmydata-tahoe-1.10.0 then start with 0 (zero):

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Conclusion:**

**On windows, you can not only follow the**\ **quickstart.rst**

**On windows, you need pre-installation of: python27,Twisted and pywin32**

**On windows, you need to run the scripts as Administrator,**

**not only an account with admin user rights.**

**On windows 64 you need additional**\ **egenix\_pyopenssl-0.13.7-py2.7-win-amd64.egg**

            
 

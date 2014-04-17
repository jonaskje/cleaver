
1. Create a folder 
2. Copy node.exe to that folder
3. Install npm to that folder
4. Make sure you have installed VS2012
5. Install JDK from Oracle
6. Set JAVA_HOME="C:\Program Files\Java\jdk1.8.0_05\"
7. Add python 2.7 (<3.0) to your PATH
8. Add jvm.dll to your path. E.g. C:\Program Files\Java\jdk1.8.0_05\jre\bin\server
9. Run: npm install -g jonaskje/cleaver --msvs_version=2012
10. Run: jkcleaver node_modules\jkcleaver\examples\test.md
11. Open apidesign.html in a Chrome browser





--------------------------------------
OLD STUFF
--------------------------------------


install node.exe

(bash) curl https://www.npmjs.org/install.sh | sh  (installs npm)

install JDK from oracle

set JAVA_HOME="c:\program files\jdk_1.8.0"

jvm.dll must be in the path. E.g. c:\program files\jdk_1.8.0\bin\server

sync jonaskje\cleaver
sync jonaskje\marked

(in marked folder) ..\Presentations\npm link --msvs_version=2012


!!! Not sure how I got this to work in the end. Had problems with NOENT errors when linking from Presentations
!!! Cleaned all Presentations\node_modules and then did a cleaver link again and then it worked.


cd cleaver
npm link --msvs_version=2012


cd Presenations
npm link <path to jonaskje\cleaver>  --msvs_version=2012




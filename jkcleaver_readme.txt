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




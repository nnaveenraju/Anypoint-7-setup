

Setup 
<br>AnypointStudio.ini
<br>
<br>

-startup
plugins/org.eclipse.equinox.launcher_1.4.0.v20161219-1356.jar

*this is a new parameter we have to add for studio to launch..

-vm
c:/progra~1/Java/jdk1.8.0_171/bin/javaw.exe
--launcher.library
plugins/org.eclipse.equinox.launcher.win32.win32.x86_64_1.1.551.v20171108-1834
-vmargs
--add-modules=ALL-SYSTEM
-Xms512m

<br>
*increase the memory size allocation
-Xmx2048m
-XX:MaxPermSize=512m
-Dosgi.instance.area.default=@user.home/AnypointStudio/studio-workspace
-Dhttps.protocols=TLSv1,TLSv1.1,TLSv1.2
-Dsun.zip.disableMemoryMapping=true
-Dequinox.resolver.revision.batch.size=1
-Dmule.testingMode=true
-Dorg.mule.tooling.runtime.args=-XX:-UseBiasedLocking
-Dorg.mule.tooling.runtime.proxyVmArgs=-Dcom.ning.http.client.AsyncHttpClientConfig.useProxyProperties=true
-Djdk.http.auth.tunneling.disabledSchemes=
-XX:ErrorFile=./studio_crash_report.log
-Dorg.mule.tooling.client.usecache=true
-Dtooling.concurrent.local.repository.enabled=false
<br>
*new param to clean the osgi settings that eclipse stores..
-Dosgi.clean=true

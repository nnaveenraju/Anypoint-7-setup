

Setup 
<br>AnypointStudio.ini
<br>
<br>

-startup<br>
plugins/org.eclipse.equinox.launcher_1.4.0.v20161219-1356.jar<br>

***this is a new parameter we have to add for studio to launch..

-vm<br>
c:/progra~1/Java/jdk1.8.0_171/bin/javaw.exe<br>
--launcher.library<br>
plugins/org.eclipse.equinox.launcher.win32.win32.x86_64_1.1.551.v20171108-1834<br>
-vmargs<br>
--add-modules=ALL-SYSTEM<br>
-Xms512m<br>

<br><br>
*increase the memory size allocation<br>
-Xmx2048m<br>
-XX:MaxPermSize=512m<br>
-Dosgi.instance.area.default=@user.home/AnypointStudio/studio-workspace<br>
-Dhttps.protocols=TLSv1,TLSv1.1,TLSv1.2<br>
-Dsun.zip.disableMemoryMapping=true<br>
-Dequinox.resolver.revision.batch.size=1<br>
-Dmule.testingMode=true<br>
-Dorg.mule.tooling.runtime.args=-XX:-UseBiasedLocking<br>
-Dorg.mule.tooling.runtime.proxyVmArgs=-Dcom.ning.http.client.AsyncHttpClientConfig.useProxyProperties=true<br>
<br>-Djdk.http.auth.tunneling.disabledSchemes=
<br>-XX:ErrorFile=./studio_crash_report.log
<br>-Dorg.mule.tooling.client.usecache=true
<br>-Dtooling.concurrent.local.repository.enabled=false
<br>
***new param to clean the osgi settings that eclipse stores..
-Dosgi.clean=true

---------------------------------------------------------------------
README-service.txt, service.bat and jbosssvc.exe are part of the
'JBoss Native Win32' distribution. They are included here to allow
JBossAS run as a Service in Windows environments.

The version used is 'JBoss Native 2.0.6 Win32' and can be downloaded from:
http://www.jboss.org/jbossweb/downloads/jboss-native/

To learn more about the JBoss Web Native connectors see:
http://www.jboss.org/jbossweb/native.html

$Id: README-service.txt 111969 2011-08-09 15:26:56Z smcgowan@redhat.com $
---------------------------------------------------------------------
The JBoss(R)* app server is Copyright 2000-2011, Red Hat Middleware LLC
and individual contributors, and is licensed under the GNU LGPL.


How to run JBoss AS as a Windows Service

JBoss AS comes with Windows service executable as part of JBossNative
that can run JBoss Application Server as service.
The service executable jbosssvc.exe transforms the run.bat and
shutdown.bat batch scripts to services. This means that any change
made to those scripts will be used both in service and command
line mode.


To install the JBoss Application Server as Windows service use
the provided service.bat batch file.

C:\> cd c:\jboss-6.1.0\bin
C:\> service.bat install

To start the JBoss Application Server as Windows service use Control pannel
or net start command. When running in service mode the console output is
redirected to the file run.log. You can inspect the file for any errors
during service startup.


C:\> net start JBAS61SVC
  The JBoss Application Server 6.1 service is starting.
  The JBoss Application Server 6.1 service was started successfully.


To stop the JBoss Application Server as Windows service use Control pannel
or net stop command. When running in service mode the console output
is redirected to the file shutdown.log. You can inspect the file for
any errors during service shutdown.


C:\> net stop JBAS61SVC
  The JBoss Application Server 6.1 service was stopped successfully.


To restart the JBoss Application Server as Windows service use Control pannel.

To remove the JBoss Application Server as Windows service use the provided
service.bat batch file.


C:\> cd c:\jboss-6.1.0\bin
C:\> service.bat uninstall


Service customization is done by editing the service.bat script.
Each command has a separate section that you can customize. The most
common customization task would be changing service names if more then
one service instances per box are required.

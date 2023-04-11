# Java-1402-Iran-Timezone-Fixer

This command fixes IRST timezone in java environment, after the government decided not to apply daylight saving to the new year of persian calendar. Hence, all preset timezone will add +0430 offset to the UTC time in new year (1402 Jalali calendar), whereas it should be +0330.

this tool provides the ability to update the IANA time zone definitions for any installed Java instance.
Download all the files and run:
$java -jar updater.jar -l file://[path]/tzdata.tar.gz

Point:
for some applications like logstash, weblogic, etc that use their own JDK, you have to check the correct path of the java executable. using simple term 'java' may use other java instances installed on the os.

for example and for logstash, run this command:
$/usr/share/logstash/jdk/bin/java -jar updater.jar -l file://[path]/tzdata.tar.gz

Use 'whereis java' to check all existing java paths in your OS.
$whereis java

Get the latest timezone database from https://www.iana.org/

Thanks to AZUL (https://www.azul.com/products/components/ziupdater-time-zone-tool/)

for Oracle tools, check out https://www.oracle.com/java/technologies/javase/tzupdater-readme.html



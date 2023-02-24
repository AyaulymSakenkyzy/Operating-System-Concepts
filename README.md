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

# TASK 2.1
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

# TASK 2.2
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

# TASK2.3
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

# TASK 3
root@kali:~# cd Downloads
root@kali:~/Downloads# wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.2.tar.xz
--2023-02-24 07:59:51--  https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.2.tar.xz
Resolving cdn.kernel.org (cdn.kernel.org)... 146.75.121.176, 2a04:4e42:8e::432
Connecting to cdn.kernel.org (cdn.kernel.org)|146.75.121.176|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 136430892 (130M) [application/x-xz]
Saving to: ‘linux-6.2.tar.xz’

linux-6.2.tar.xz    100%[===================>] 130.11M  11.7MB/s    in 10s     

2023-02-24 08:00:02 (12.9 MB/s) - ‘linux-6.2.tar.xz’ saved [136430892/136430892]

root@kali:~/Downloads# ls
 compat-wireless-2010-06-26-p           putty.exe
 compat-wireless-2010-06-26-p.tar.bz2  'school(1).exe'
 Kage.0.1.1-beta_linux.AppImage        'school(2).exe'
 Kage.Setup.0.1.1-beta_Win64.exe        school.exe
 linux-6.2.tar.xz
root@kali:~/Downloads#

# 3.1
root@kali:~# cd Downloads
root@kali:~/Downloads# wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.2.tar.xz
--2023-02-24 07:59:51--  https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.2.tar.xz
Resolving cdn.kernel.org (cdn.kernel.org)... 146.75.121.176, 2a04:4e42:8e::432
Connecting to cdn.kernel.org (cdn.kernel.org)|146.75.121.176|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 136430892 (130M) [application/x-xz]
Saving to: ‘linux-6.2.tar.xz’

linux-6.2.tar.xz    100%[===================>] 130.11M  11.7MB/s    in 10s     

2023-02-24 08:00:02 (12.9 MB/s) - ‘linux-6.2.tar.xz’ saved [136430892/136430892]

root@kali:~/Downloads# ls
 compat-wireless-2010-06-26-p           putty.exe
 compat-wireless-2010-06-26-p.tar.bz2  'school(1).exe'
 Kage.0.1.1-beta_linux.AppImage        'school(2).exe'
 Kage.Setup.0.1.1-beta_Win64.exe        school.exe
 linux-6.2.tar.xz
root@kali:~/Downloads# ^C
root@kali:~/Downloads# mkdir linux_kernel
root@kali:~/Downloads# mv linux-6.2.tar.xz ~/Downloads/linux_kernel
root@kali:~/Downloads# cd linux_kernel
root@kali:~/Downloads/linux_kernel# ls
linux-6.2.tar.xz
root@kali:~/Downloads/linux_kernel# tar xvf linux-6.2.tar.xz

# 3.2
root@kali:~/Downloads/linux_kernel# ls
linux-6.2  linux-6.2.tar.xz
root@kali:~/Downloads/linux_kernel# ls -a
.  ..  linux-6.2  linux-6.2.tar.xz
root@kali:~/Downloads/linux_kernel# du -sh
1.6G .
root@kali:~/Downloads/linux_kernel# sudo apt-get install git fakeroot build-essential ncurses-dev xz-utilis libssl-dev bc flex libelf-dev bison libncurses-dev rsync gcc libncurses5-dev
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Note, selecting 'libncurses-dev' instead of 'ncurses-dev'
E: Unable to locate package xz-utilis
root@kali:~/Downloads/linux_kernel# sudo update-grub
Generating grub configuration file ...
Found theme: /boot/grub/themes/kali/theme.txt
Found background image: /usr/share/images/desktop-base/desktop-grub.png
Found linux image: /boot/vmlinuz-5.15.0-kali3-amd64
Found initrd image: /boot/initrd.img-5.15.0-kali3-amd64
done

# 3.3
root@kali:~/Downloads/linux_kernel# sudo apt update
Get:1 http://kali.download/kali kali-rolling InRelease [41.2 kB]
Get:2 http://kali.download/kali kali-last-snapshot InRelease [41.2 kB]
Get:3 http://kali.download/kali kali-rolling/main i386 Packages [19.2 MB]
Get:4 http://kali.download/kali kali-rolling/main amd64 Packages [19.5 MB]
Get:5 http://kali.download/kali kali-rolling/main amd64 Contents (deb) [45.4 MB]
Get:6 http://kali.download/kali kali-rolling/main i386 Contents (deb) [43.8 MB]                                   
Get:7 http://kali.download/kali kali-rolling/contrib amd64 Packages [116 kB]                                      
Get:8 http://kali.download/kali kali-rolling/contrib i386 Packages [100 kB]                                       
Get:9 http://kali.download/kali kali-rolling/contrib amd64 Contents (deb) [172 kB]                                
Get:10 http://kali.download/kali kali-rolling/contrib i386 Contents (deb) [142 kB]                                
Get:11 http://kali.download/kali kali-rolling/non-free amd64 Packages [222 kB]                                    
Get:12 http://kali.download/kali kali-rolling/non-free i386 Packages [179 kB]                                     
Get:13 http://kali.download/kali kali-rolling/non-free i386 Contents (deb) [883 kB]                               
Get:14 http://kali.download/kali kali-rolling/non-free amd64 Contents (deb) [931 kB]                              
Fetched 131 MB in 29s (4,514 kB/s)                                                                                
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
2172 packages can be upgraded. Run 'apt list --upgradable' to see them.

root@kali:~/Downloads/linux_kernel# sudo apt install mainline
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done

# 3.4
root@kali:~/Downloads/linux_kernel# uname -r
5.15.0-kali3-amd64
root@kali:~/Downloads/linux_kernel# uname -a
Linux kali 5.15.0-kali3-amd64 #1 SMP Debian 5.15.15-2kali1 (2022-01-31) x86_64 GNU/Linux

# 3.5
root@kali:~/Downloads/linux_kernel# sudo su student
┌──(student㉿kali)-[/root/Downloads/linux_kernel]
└─$ cd

┌──(student㉿kali)-[~]
└─$ sudo su

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for student: 
student is not in the sudoers file.  This incident will be reported.

# 3.6
#include <linux/init.h>
#include <linux/module.h>

MODULE_LICENSE("GPL");
MODULE_AUTHOR("DIANA");
MODULE_DESCRIPTION("Hi student - Linux Kernel Module");

static int __init hi_init(void){
        printk(KERN_INFO "Hi student\n");
        return 0;
}

static void __exit hello_exit(void){
        printk(KERN_INFO "Bye student\n");
}
 
module_init(hello_init);
module_exit(hello_exit);

#3.7
obj-m += read_write.o

all:
 make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
 make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
 


 #include <linux/module.h>
#include <linux/init.h>
#include <linux/fs.h>
#include <linux/cdev.h>
#include <linux/uaccess.h>

MODULE_LICENSE("GPL");
MODULE_AUTHOR("Diana");
MODULE_DESCRIPTION("Imitation Device Callbacks - Linux Kernel Module");

static char buffer[255];
static int buffer_pointer = 0;

static dev_t my_device_nr;
static struct class *my_class;
static struct cdev my_device;

#define DRIVER_NAME "dummydriver"
#define DRIVER_CLASS "MyModuleClass"

static ssize_t driver_read(struct file *File, char *user_buffer, size_t count, loff_t *offs) {
 int to_copy, not_copied, delta;

 to_copy = min(count, buffer_pointer);

 not_copied = copy_to_user(user_buffer, buffer, to_copy);

 delta = to_copy - not_copied;

 return delta;
}

static ssize_t driver_write(struct file *File, const char *user_buffer, size_t count, loff_t *offs) {
 int to_copy, not_copied, delta;

 to_copy = min(count, sizeof(buffer));

 not_copied = copy_from_user(buffer, user_buffer, to_copy);
 buffer_pointer = to_copy;

 delta = to_copy - not_copied;

 return delta;
}

static int driver_open(struct inode *device_file, struct file *instance) {
 printk("dev_nr - open was called!\n");
 return 0;
}

static int driver_close(struct inode *device_file, struct file *instance) {
 printk("dev_nr - close was called!\n");
 return 0;
}

static struct file_operations fops = {
 .owner = THIS_MODULE,
 .open = driver_open,
 .release = driver_close,
 .read = driver_read,
 .write = driver_write
};

static int __init ModuleInit(void) {
 int retval;
 printk("Hello, Kernel!\n");

 if( alloc_chrdev_region(&my_device_nr, 0, 1, DRIVER_NAME) < 0) {
  printk("Device Nr. could not be allocated!\n");
  return -1;
 }
 printk("read_write - Device Nr. Major: %d, Minor: %d was registered!\n", my_device_nr >> 20, my_device_nr && 0xfffff);

 if((my_class = class_create(THIS_MODULE, DRIVER_CLASS)) == NULL) {
  printk("Device class can not be created!\n");
  goto ClassError;
 }

 if(device_create(my_class, NULL, my_device_nr, NULL, DRIVER_NAME) == NULL) {
  printk("Can not create device file!\n");
  goto FileError;
 }

 cdev_init(&my_device, &fops);

 if(cdev_add(&my_device, my_device_nr, 1) == -1) {
  printk("Registering of device to kernel failed!\n");
  goto AddError;
 }

 return 0;
AddError:
 device_destroy(my_class, my_device_nr);
FileError:
 class_destroy(my_class);
ClassError:
 unregister_chrdev_region(my_device_nr, 1);
 return -1;
}

static void __exit ModuleExit(void) {
 cdev_del(&my_device);
 device_destroy(my_class, my_device_nr);
 class_destroy(my_class);
 unregister_chrdev_region(my_device_nr, 1);
 printk("Goodbye, Kernel\n");
}

module_init(ModuleInit);
module_exit(ModuleExit);


obj-m += read_write.o

all:
 make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
 make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

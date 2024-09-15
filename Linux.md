
## توزيعات لينكس

| **التوزيعة**          | **الوصف**                                                | **الأمثلة**                                    |
|-----------------------|----------------------------------------------------------|------------------------------------------------|
| **Ubuntu**            | توزيعة سهلة للمبتدئين، تدعم الكثير من البرمجيات.       | استخدام كأول توزيعة لينكس، مناسبة للأجهزة الشخصية. |
| **Fedora**            | تحتوي على أحدث البرمجيات، مناسبة للتجربة الجديدة.    | تستخدم في بيئات التطوير والتجربة.            |
| **CentOS**            | نسخة مجانية من Red Hat، مخصصة للخوادم.                 | إدارة الخوادم وإعداد البنية التحتية.         |
| **Kali Linux**        | متخصصة في اختبار الأمان والاختراق.                      | يستخدمها المتخصصون في الأمن السيبراني.      |
| **Parrot Security OS** | توزيعة أخرى للأمان وحماية البيانات.                   | بديل لـ Kali Linux، يحتوي على أدوات حماية إضافية. |

---

## مديري الحزم

| **مدير الحزم** | **التوزيعات المدعومة** | **الأوامر الشائعة**                                          | **الأمثلة**                          |
|----------------|------------------------|--------------------------------------------------------------|--------------------------------------|
| **apt-get**    | Debian، Ubuntu         | `apt-get install package` <br> `apt-get update`              | `apt-get install vim` <br> `apt-get update` |
| **yum**        | Red Hat، CentOS        | `yum install package` <br> `yum update`                      | `yum install wget` <br> `yum update` |
| **dnf**        | Fedora                 | `dnf install package` <br> `dnf update`                      | `dnf install htop` <br> `dnf update` |
| **pacman**     | Arch Linux             | `pacman -S package` <br> `pacman -Syu`                       | `pacman -S git` <br> `pacman -Syu` |

---

## إدارة الملفات والمجلدات

| **الأمر**   | **الوصف**                                  | **الأمثلة**                                            |
|-------------|--------------------------------------------|--------------------------------------------------------|
| `ls`        | عرض الملفات والمجلدات.                     | `ls` <br> `ls -l` <br> `ls -a` <br> `ls -lh`          |
| `cd`        | تغيير المجلد.                             | `cd /var` <br> `cd ..` <br> `cd ~/Documents`          |
| `cp`        | نسخ الملفات والمجلدات.                     | `cp file1.txt file2.txt` <br> `cp -r dir1/ dir2/`    |
| `mv`        | نقل أو إعادة تسمية الملفات.                | `mv file1.txt /otherfolder/` <br> `mv oldname.txt newname.txt` |
| `rm`        | حذف الملفات.                             | `rm file1.txt` <br> `rm -r folder/` <br> `rm -f file.txt` |
| `mkdir`     | إنشاء مجلد جديد.                           | `mkdir newfolder` <br> `mkdir -p parentfolder/childfolder` |
| `rmdir`     | حذف مجلد فارغ.                             | `rmdir emptyfolder` <br> `rmdir -p parentfolder/childfolder` |
| `find`      | البحث عن ملفات.                           | `find /home -name report.txt` <br> `find / -type f -size +100M` |
| `grep`      | البحث داخل محتويات الملفات.               | `grep "error" logfile.txt` <br> `grep -r "searchterm" /directory` |
| `chmod`     | تغيير صلاحيات الوصول للملفات.              | `chmod +x script.sh` <br> `chmod 644 file.txt`        |
| `chown`     | تغيير مالك الملف.                          | `chown user file.txt` <br> `chown user:group file.txt` |
| `df`        | عرض معلومات عن استخدام القرص.              | `df -h` <br> `df -Th`                                |
| `du`        | عرض حجم الملفات والمجلدات.                 | `du -sh myfolder` <br> `du -ah`                        |

---

## العمليات والخدمات

| **الأمر**     | **الوصف**                              | **الأمثلة**                                          |
|---------------|----------------------------------------|------------------------------------------------------|
| `ps`          | عرض العمليات الجارية.                 | `ps aux` <br> `ps -ef` <br> `ps -aux | grep processname` |
| `top`         | مراقبة الأداء.                        | `top`                                               |
| `htop`        | عرض متقدم للعمليات.                   | `htop`                                              |
| `systemctl`   | إدارة الخدمات في الأنظمة الحديثة.     | `systemctl start httpd` <br> `systemctl status sshd` <br> `systemctl restart nginx` |
| `service`     | إدارة الخدمات في الأنظمة الأقدم.       | `service nginx start` <br> `service apache2 stop` <br> `service mysql restart` |

---

## النسخ الاحتياطي والصيانة

| **الأمر**     | **الوصف**                                    | **الأمثلة**                                          |
|---------------|----------------------------------------------|------------------------------------------------------|
| `tar`         | إنشاء وضغط النسخ الاحتياطية.                | `tar -czvf backup.tar.gz /path/to/data` <br> `tar -xzvf backup.tar.gz` |
| `rsync`       | مزامنة الملفات والمجلدات.                    | `rsync -av /source/ /destination/` <br> `rsync -avz /local/path remote:/remote/path` |
| `cron`        | جدولة المهام التلقائية.                     | `crontab -e` <br> `0 2 * * * /path/to/backup.sh` <br> `crontab -l` |

---

## الأمان

| **الأمر**      | **الوصف**                                    | **الأمثلة**                                          |
|----------------|----------------------------------------------|------------------------------------------------------|
| `firewalld`    | إدارة الجدار الناري.                        | `firewall-cmd --add-port=80/tcp --permanent` <br> `firewall-cmd --reload` |
| `iptables`     | إدارة الجدار الناري.                        | `iptables -A INPUT -p tcp --dport 22 -j ACCEPT` <br> `iptables -A INPUT -p tcp --dport 80 -j ACCEPT` |
| `ufw`          | أداة أبسط لإدارة الجدار الناري.              | `ufw allow 22` <br> `ufw deny 80` <br> `ufw status` |
| `SELinux`      | تعزيز الأمان عبر سياسات أمان إضافية.          | `sestatus` <br> `setenforce 1` <br> `setenforce 0` |

---

## الملفات والمجلدات

| **المجلد**       | **الوصف**                                   | **الأمثلة**                                            |
|------------------|---------------------------------------------|--------------------------------------------------------|
| `/home`          | يحتوي على الملفات الشخصية للمستخدمين.     | `/home/username`                                     |
| `/etc`           | يحتوي على ملفات الإعدادات.                 | `/etc/network/interfaces`                           |
| `/var`           | يحتوي على ملفات البيانات المتغيرة.        | `/var/log/`                                          |
| `/tmp`           | يحتوي على الملفات المؤقتة.                 | `/tmp`                                               |
| `/usr`           | يحتوي على البرمجيات والمكتبات.             | `/usr/bin/` <br> `/usr/lib/`                         |


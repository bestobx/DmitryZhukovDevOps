Дмитрий Жуков. Домашнее задание#1

1)ls

[zhukov@epam-workstation1 ~]$ ls /usr/share/man/*/*config*
/usr/share/man/man1/pkg-config.1.gz
/usr/share/man/man5/config.5ssl.gz
/usr/share/man/man5/config-util.5.gz
/usr/share/man/man5/selinux_config.5.gz
/usr/share/man/man5/ssh_config.5.gz
/usr/share/man/man5/sshd_config.5.gz
/usr/share/man/man5/x509v3_config.5ssl.gz
/usr/share/man/man8/authconfig.8.gz
/usr/share/man/man8/authconfig-tui.8.gz
/usr/share/man/man8/chkconfig.8.gz
/usr/share/man/man8/grub2-mkconfig.8.gz
/usr/share/man/man8/iprconfig.8.gz
/usr/share/man/man8/lvm-config.8.gz
/usr/share/man/man8/lvmconfig.8.gz
/usr/share/man/man8/lvm-dumpconfig.8.gz
/usr/share/man/man8/sys-unconfig.8.gz

[zhukov@epam-workstation1 ~]$ ls /usr/share/man/man{1,7}/*system*
/usr/share/man/man1/systemctl.1.gz
/usr/share/man/man1/systemd.1.gz
/usr/share/man/man1/systemd-analyze.1.gz
/usr/share/man/man1/systemd-ask-password.1.gz
/usr/share/man/man1/systemd-bootchart.1.gz
/usr/share/man/man1/systemd-cat.1.gz
/usr/share/man/man1/systemd-cgls.1.gz
/usr/share/man/man1/systemd-cgtop.1.gz
/usr/share/man/man1/systemd-delta.1.gz
/usr/share/man/man1/systemd-detect-virt.1.gz
/usr/share/man/man1/systemd-escape.1.gz
/usr/share/man/man1/systemd-firstboot.1.gz
/usr/share/man/man1/systemd-firstboot.service.1.gz
/usr/share/man/man1/systemd-inhibit.1.gz
/usr/share/man/man1/systemd-machine-id-commit.1.gz
/usr/share/man/man1/systemd-machine-id-setup.1.gz
/usr/share/man/man1/systemd-notify.1.gz
/usr/share/man/man1/systemd-nspawn.1.gz
/usr/share/man/man1/systemd-path.1.gz
/usr/share/man/man1/systemd-run.1.gz
/usr/share/man/man1/systemd-tty-ask-password-agent.1.gz
/usr/share/man/man7/lvmsystemid.7.gz
/usr/share/man/man7/systemd.directives.7.gz
/usr/share/man/man7/systemd.generator.7.gz
/usr/share/man/man7/systemd.index.7.gz
/usr/share/man/man7/systemd.journal-fields.7.gz
/usr/share/man/man7/systemd.special.7.gz
/usr/share/man/man7/systemd.time.7.gz


2)find

[zhukov@epam-workstation1 ~]$ find /usr/share/man -name '*help*'     
/usr/share/man/man1/help.1.gz
/usr/share/man/man8/pwhistory_helper.8.gz
/usr/share/man/man8/mkhomedir_help

[zhukov@epam-workstation1 ~]$ find /usr/share/man -name 'conf*'     
/usr/share/man/man5/config.5ssl.gz
/usr/share/man/man5/config-util.5.gz

#При помощи find можно, например, удалить все текстовые файлы 

[zhukov@epam-workstation1 ~]$ ls /tmp
file1.txt  file2.txt  ks-script-k4Olb9  yum.log
[zhukov@epam-workstation1 ~]$ find /tmp -type f -name "*.txt" -exec rm -f {} \;
[zhukov@epam-workstation1 ~]$ ls /tmp
ks-script-k4Olb9  yum.log

 
3)tail, head

[zhukov@epam-workstation1 ~]$ tail -2 /etc/fstab 
UUID=71cda756-097e-42cf-aab4-8d00c5204acc /boot                   xfs     defaults        0 0
/dev/mapper/centos-swap swap                    swap    defaults        0 0


[zhukov@epam-workstation1 ~]$ head -7 /etc/yum.conf 
[main]
cachedir=/var/cache/yum/$basearch/$releasever
keepcache=0
debuglevel=2
logfile=/var/log/yum.log
exactarch=1
obsoletes=1

[zhukov@epam-workstation1 ~]$ tail -20000 /etc/fstab | wc -l
11


4)touch

[zhukov@epam-workstation1 ~]$ touch file_name1.md file_name2.md file_name3.md
[zhukov@epam-workstation1 ~]$ ls
file_name1.md  file_name2.md  file_name3.md

5)cd

[zhukov@epam-workstation1 ~]$ cd /mnt
[zhukov@epam-workstation1 mnt]$ cd -
/home/zhukov
[zhukov@epam-workstation1 ~]$ cd /mnt
[zhukov@epam-workstation1 mnt]$ cd
[zhukov@epam-workstation1 ~]$ cd /mnt
[zhukov@epam-workstation1 mnt]$ cd ~
[zhukov@epam-workstation1 ~]$ cd /home/zhukov/

6)

[zhukov@epam-workstation1 ~]$ mkdir new in-process processed && mkdir in-process/thread{0..2} && touch new/data{00..99} && cp new/data{00..33} in-process/thread0/ && cp new/data{34..66} in-process/thread1/ && cp new/data{67..99} in-process/thread2/ && ls -R in-process && mv in-process/thread*/* processed && ls -R in-process && [ `ls new | wc -l` == `ls processed | wc -l` ] && rm new/*
in-process:
thread0  thread1  thread2

in-process/thread0:
data00  data04  data08  data12  data16  data20  data24  data28  data32
data01  data05  data09  data13  data17  data21  data25  data29  data33
data02  data06  data10  data14  data18  data22  data26  data30
data03  data07  data11  data15  data19  data23  data27  data31

in-process/thread1:
data34  data37  data40  data43  data46  data49  data52  data55  data58  data61  data64
data35  data38  data41  data44  data47  data50  data53  data56  data59  data62  data65
data36  data39  data42  data45  data48  data51  data54  data57  data60  data63  data66

in-process/thread2:
data67  data70  data73  data76  data79  data82  data85  data88  data91  data94  data97
data68  data71  data74  data77  data80  data83  data86  data89  data92  data95  data98
data69  data72  data75  data78  data81  data84  data87  data90  data93  data96  data99
in-process:
thread0  thread1  thread2

in-process/thread0:

in-process/thread1:

in-process/thread2:
[zhukov@epam-workstation1 ~]$ 

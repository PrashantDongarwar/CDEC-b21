# CDEC-b21

Introduction 

Linux is a open source operating system:

O/S:-

1. Manages the hardware
2. It proivides env. to run our applications
3. It is mediator between user and hardware.
4. it converts high level lang. to low level language
   high level --- human redable, script, java
   low level language ----- binary (0,1)


   1991 - Linus torvald 
   GNU---- richard stallman 
   unix --- Linux (we can download it oveer the internet) --- open source

   Types of operating system:

   1. Desktop os ---- personal use, browsing, gaming, editing, etc
          ex. windows, (90-95%) ubuntu desktop, kali
           GUI-- graphical user interface

 2. server O/S ------ web hosting, network file sharing
          ex. Linux o/s (90%)
            ubuntu, centos, kali linux, debian, fedora, RHEL, windows 19
            CLI-- command line inetrface.


 Development of O/S;

 1. single user single tasking ------- ex- msdos
 2. single user multi tasking ------- desktop os -- windows 
 3. multi user multi tasking ------- server os --linux o/s


Architecture of Linux:-

Application Layer: - Users interact with the system through varies applications such as office, games, 
etc. These applications run in outer layer of architecture. 
 
Shell: - Shell provides environment to run any application. It provides interface to the user to interact 
with hardware. . 
 
Kernel: - Kernel is the program which actually communicates with the hardware. it is a core part of sytem. 
 Combining shell and kernel forms Operating System. Heart of system. We can say that it converts higher level language to lower level language
 
Hardware: - All the hardware components such as motherboard, CPU, hard disk, etc. are comes under 
this layer.  


1. Physicaly
2. Online----- labex 
3. AWS 


basic commands

1. ls -------- list the content of directory
  ls -l -------- it shows more information of files and directories
2. mkdir ------- tto create the directory
3. rm 
4. cp 
5. mv
6. touch ------ to create the empty file
7. cd --------- for change the directory
8. pwd-------- print working directory (present working directory)
9. tail 
10. grep
11. head 
12. clear ---------- clear the screen 
       (ctrl+l)
13. cal ------ it shows the calendar 
      cal -3 ----- it will show 3 months cale.
      cal march 2025  
14. date -------- current date
      date -s "22:10 6 dec 2024"


steps to download cal command
 - apt update
 - apt install util-linux
 - apt install ncal


command promp:

root            @          67531857098fa2ceb3702fe8:     ~                         #
login user   saperator      hostname(machine name)    present directory    it shows root user login
                                                                           local user ($)



Navigating the filesystem

1) Absolute path -------- full path    ex: /home/labex/project
                                           /a/b/c/d/e

                                    
2) Relative path -------- ex: cd  ./d/e
                              cd ./project


A..........B.........C.......D........E
country   state     city    village  home
          cd ./d


touch file.txt--------- create file at current location
touch /home/data.txt----- create file inside home directory 
touch project.txt project1.txt-------- create multiple files in sigle command  
touch /mnt/imp.txt /root/abc.txt /home/xyz------ create multiple files in different location
touch /root/{data.txt,file1.txt,projectfile.txt}------- create multiple file at different location
touch file{1..20}.txt-------- create 20 files with same name in single command
touch .imp.txt-------- to create hidden file
ls -a -------- to list hidden files
mkdir demo -------- to create directory at current location

task: Do the same practice with mkdir command

File operation :

READ :-
 1) cat  ----------- use to read the file which have small amount od data
 2) more ----------- you can scroll the data downword using enter command, but you cant scroll updard
 3) less ----------- you can scroll upward and downward using upper arrow key and lower arrow key. come out using ctrl+z
 4) head ----------- by deafult it will show top 10 lines
    head -n <no> <file name>
    ex : head -n 5 /etc/passwd --------- it will show top 5 lines
5) tail ------------ by deafult it will show bottom 10 lines
    tail -n 15 /etc/passwd ------- it will show bottom 5 lines



COPY :-
 
command ---
     cp <options> <source> <destination>
       
  options :
       -r ------- (recursive) for copy the directory
       -f ------- for forcefully
       -v ------- (verbose/view)     
ex: cp /root/file.txt /home/   ----------copy file.txt from root to home dir
    cp -rv /root/dir1 /home/   ---------- copy directory from root to home

REMOVE :- 
      rm <options>  <file name>     
ex :  rm file.txt --------- remove the file
      rm -rvf <directory name> 
      rmdir dir1------- remove the empty directory

MOVE : 
    mv <source> <destination>
ex: mv /mnt/project /home/ -------- move project dir from mnt to home
    mv /home/file.txt /root/ ------ move file.txt from home root
    mv flowor.txt flower.txt ------- we can rename the filename
    mv /root/flowor.txt /home/flower.txt


Hierachy Of linux file system :
1) /root ------- root directory is a home directory of root user *
2) /home ------ it is a home directory of local userb*
3) /etc ------- it stores all configurations files of system and services *
4) /bin ------- it stores binary files, binary file means nothing but our commands (local user commands)
5) /sbin ------ it srores system binary executable files, commands----- (root user command)
6) /var ------ it stores variable data such as, mail, logs, messages etc.... *
7) /lib32 ------ library file information, support 32 bit commands
8) /lib64 ------ library file information, 64 bit supporting files 
9) /boot ------- it store boot loader and other booting files that helps to start our system
10) /dev ------- it stores device realated information, usb drives, printer, 
11) /media ----- information of removable devices, card reader, pendrives, flopy disk
12) /sys ------- system realed information
13) /run ------ store the infirmation of all runnig devices
14) /proc ----- it stores the process related information, it store information related RAM and CPU
15) /tmp ------ it stores temporary file for 10 days
16) /usr ------ it store user related information, man pages
17) /srv ------ it stores service realated information
18) /mnt ------ it store mount point for our storage devices ex : hard disk*
19) /opt ----- optional directory, addon services information 

1.boot
2.bin
3.dev
4.etc
5.home
6.lib32
7.lib64
8.media
9.mnt
10.opt
11.proc
12.root
13.run
14.sbin
15.sys
16.srv
17.tmp
18.var
19.usr

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


touch file.txt --------- create file at current location
touch /home/data.txt ----- create file inside home directory   
touch project.txt project1.txt -------- create multiple files in sigle command   
touch /mnt/imp.txt /root/abc.txt /home/xyz  ------ create multiple files in different locations
touch /root/{data.txt,file1.txt,projectfile.txt} ------- create multiple file at different location
touch file{1..20}.txt  -------- create 20 files with same name in single command
touch .imp.txt  -------- to create hidden file
ls -a -------- to list hidden files
mkdir demo -------- to create directory at current location

task: Do the same practice with mkdir command

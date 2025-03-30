## Introduction 

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
with hardware. . Bash shell, Cshell, zshell, cornshell
 
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
15. hostname --------- shows the machine name


steps to download cal command
 - apt update
 - apt install util-linux
 - apt install ncal


command promp:

   root            @          67531857098fa2ceb3702fe8:      ~                         #
login user      saperator      hostname(machine name)    present directory    it shows root user login or
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
mkdir /project ------- directory will be crreated inside the / directory
mkdir /project/demo ------- demo directory will be created inside practice dir.
mkdir -p /root/project/practice ---------- create parent directory 
task: Do the same practice with mkdir command

## File operation :

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
    cp -rvf /root/* /mnt/      ---------- copy all the data inside /mnt direcotry from /root

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
    mv /root/flowor.txt /home/flower.txt ------ move and rename at same time


## Hierachy Of linux file system :
1) /root ------- root directory is a home directory of root user *
2) /home ------ it is a home directory of local users*
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
18) /mnt ------ it store mount point for our storage devices ex : hard disk *
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
18.usr
19.var

## Editior in Linux :

In windows :- note pad, m. world, vs code

In Linux :- 
  *Graphical editior --- gedit, kedit

  *CLI editiors ------- pico, nano, vi, vim

  **vim editor 
    1) command mode
    2) Insert mode
    3) Execution mode
    4) Visual mode

    #1) Command mode :
       1. G -------- move cursor at end of file, bottom of the file
       2. gg ------- move cursor at top of the file
       3. yy ------- for copy the line where your cursor is present
       4. <number>yy -- copu no of lines 
       5. yw ------- copy the single world
       6. <number>yw copy no of words
       7. p ------- for paste the line to below the cursor
       8. P ------- paste the line at top of cursor
       9. dd ------ for delete the line
       10. <n>dd ----- delete nimbers of line
       11. dw -------- delete the word 
       12. <n>dw ----- delete the numbers of words
       13. cc ------ for cut the line
       14. <n>cc ------ cut number of lines
       15. cw ------- for cut the single word
       16. <n>cw ------ for cut the multiple words
       17. /<word> ----- search the perticular word
               n ---- move forward 
               N ---- move backward
       18. u -------- undo the changes
       19. ctrl+r ------- redo the changes

    #2) Insert mode : 
       we can edit the data manually
       1. i ------- to inster into inser mode 
       2. I ------- inser text at start of the line
       3. a 
       4. A
       5. o 
       6. O  
       7. r  
       8. R 

    #3) Execution mode : 
       - Type ":" to insert into execution mode
       1. :q ------ quit without saving the file
       2. :q! ------ quit forcefully without saving the file 
       3. :w ------- save the changes and stay in file
       4. :wq or :x or :exit ------ save the changes and quit the file
       5. :wq! or :x! ------ save the change and quit the file forcefully
       6. :set nu ------- set line numbers
       7. :set nonu ------ remove the line numbers
       8. :/<word> ------ search the word
       9. :set hlsearch ---- highlight the search word
       10 :nohl -------- remove the highlighting
       11. :%s/<oldword>/<newword>/g ------ find the word and replace it with new word
       12. :!touch /home/file.txt -------- execute any command on terminal without leaving the editior

    #4) Visual mode :
       - V --------- select line by line
       - v --------- slect character by character

         y,d,c -------- for copy,delete,cut
      
      Redirectors :
      1) > ----- single redirector  ------ (overwrite the data)
      2) >> ---- double redirector  ------ (append the data)
      3) &> ---- and redirector
      $) 2> ---- two redirector 

      task : copy data from one file to another file with overwrite
             copy data from one file to another file without overwrite

## Topic : Managing Users and Permissions in Linux :-

       A user is a person who utilizes a computer or network service. Linux is said to be secure 
       because one user cannot access files of other user without its permission. There are three types of user, 

       1. Super user/root user: Super users are those users who has all privileges of Linux system. On all 
          Linux systems, by default there is the user root, also known as the super user. This account is used for 
          managing Linux. Root, for instance, can create other user accounts on the system. For some tasks, 
          root privileges are required. Some examples are installing software, managing users, and creating 
          partitions on disk devices.  

       2. System user: System accounts are used by the services in Linux system. These 
          accounts or users generally created when services are installed in system. 

       3. Standard user(Local user): local user accounts or standard user accounts are for the people who 
          need to work on a system and who need limited access to the resources on that system. These user 
          accounts typically have a password that is used for authenticating the user to the system.

    commands: 
        useradd <username> --------- to add the user
        adduser <username> --------- add user with user information
        userdel <username> --------- delete the user
        userdel --remove <username> ----- remove user with its home direcotry
        su - <username>    --------- for switching between users
        su <username>  ----------- switch user but stay in present directory
        

   #Files get affect after useradd in the system :

   1. /home  ------------ by deafult directory get created with user name
   2. /var/spool/mail
   3. skeleton files --
            .bash_logout ----- if this file is missing our user cant be able to logout from the system
            .bash_profile----- if this file is missing, home directory will not be assigned to new user
            .bashrc   -------- if this file is missing the user will not able to login in the system
   
   
   4. /etc/passwd --- user information

           ashwini:       x:                 1000:   1000:  ,,123456789,,DevOps engineer:  /home/ashwini:     /bin/bash      
         (user name) (encrypted password)   (UID)   (GID)         (comment)               (home directory)   (user login shell) 
         
         root user ------UID------ 0
         system user ----UID range ---- 1-999
         local user -----UID range ---- 1000-

         passwd <username> ------ provide password to user
         
      commands for user modifications: 
         usermod <option> <parameter> <username>

        1) usermod -l <new_name> <old_name>  
        2) usermod -u 2000 nikita     -------- for change the userid UID
        3) usermod -c "devops engineer" nikita ------- change the comment
        4) usermod -d /mnt <user_name> -------- chnage home dir of user to mnt
        5) usermod -s /bin/sh <user_name> ----- change user login shell
        6) usermod -L <user_name> ------ Lock user account
        7) usermod -U <user_name> ------ unlock user account


   5. /etc/shadow 
       ----- user passowrd informaton

      ubuntu:$y$j9T$KBrdN4tKMbqQGaWziO0f50$s2fELyTr6Vl8gaRR42Woq3uHGIQwE4Y9U.5B/gmU6C3:20182:10:90:10:30:20333:
            
      1. Username: This is a unique name for the user. User names are important to match a 
         user to his password. On Linux, there can be no spaces in the user name. 
      2. Encrypted password: This field contains all that is needed to store the password in a secure way. 
      3. Days since Jan 1, 1970, that the password was last changed: Many things on Linux 
         refer to this date, which on Linux is considered the beginning of days. 
      4. Days before password may be changed: This is minimum age of password. That means user cannot change password,
         before the mentioned days, after immediately changing the password. Typically this field is set to the value 0. 
      5. Days after which password must be changed: This field contains the maximal validity 
         period of passwords or maximum age of password. User must have to change their password after mentioned days. 
         By default it is set to 99999 days. 
      6. Days before password is to expire that user is warned: This field is used to warn a 
         user when a forced password change is upcoming. By default it is set to 7 days. 
      7. Days after password expires that account is disabled: Use this field to enforce a 
         password change. After password expiry, users can no longer log in. 
      8. Days since Jan 1, 1970, that account is disabled: An administrator can set this field to 
         disable an account. This is typically a better approach than removing an account, as 
         all associated properties and files of the account will be kept, but it can be used no 
         longer to authenticate on your server. 
      9. For future use: This is reserved field for future use. 

commands :
   syntax; 
   chage <option> <parameter> <username>

   chage -l <username> ------- list the password onformation
   chage -m <username> ------- change minimum days between password change
   chage -M <username> ------- maximum password age
   chage -W <username> ------- warning days
   chage -I <username> ------- password inactive days
   chage -E <username> ------- account expired


  6. /etc/group  ------ it provide information about groups
      TCS              :x                   :5001        :
    (group name)  (encrypted password)      (GID)        (group members)

   commands :
    groupadd <groupname>  ------ for adding the group in system
    groupadd -g 2003 TATA ------ assigne perticular group id during creating the group
    groupmod <option> <parameter> <groupname>  ------------- modifyning the group
    groupmod -g 4001 TCS  -------- changing the group id
    groupmod -n Wipro TCS -------- change the group name
        
  7. /etc/gshadow ----- group password information, admin

    TATA           :!                       :            :
   (group name)  (encrypted password)  (admin name)   (group memebers)

   gpasswd <groupname> ------ provide password to group
   gpasswd -A <username> <groupname> ------ assign user as admin of group
   gpasswd -A "" <groupname>  ---------- remove a user as the administrator of a group

   command to add user in group
   gpasswd -a <username> <groupname>
   gpasswd -M <username,username,username> <groupname>
   gpasswd -d <username> <groupname> ------- removing the user from group
   usermod -G <groupname> <username>
   useradd -G <groupname> <username> ------- add user to group at a time of user creation
   groupdel <groupname> ----- to delete the group


## Linux File system security 
commnad 
 ls -l or ll

    d             rwxr-xr-x       2            root          root                   6       Jun 27 22:20       srv
(type of file) (permossions)  (Link count) (owner of file) (group owner of file) (size) (date of creation)  (file name)


1) user define files: 
    1. Normal file (-)
    2. Directory (d)
    3. Link file (l)

2) system define files:
   1. block device file (b)
   2. Character device file (c)
   3. Socket file (s)
   4. Pipe file (p)


r ----- read
w ----- write
x ----- execute

rwx                    r-x            --x
(owner of file)   (group owner)   (other users)
    u                 g               o


for directory :
r (read)  ------- ls 
w (write) ------- touch, mkdir, rm, cp, mv
x (execute) ----- cd


for file :
r (read) ------- cat, more, less, head, tail, vim 
w (write) ------ edit(vim), rm, cp, mv, redirect
x (execute) ---- commands, scripts 

Practical : -Login with root user
            -Create file with some data in /home directory (Owner and group Owner of file must be root user)
            -Switch to loacal user (ex. ubuntu)
            -As per permission check which actions he can performed
            -Change permissio using sudo
            
chmod u-r <filename/directoryname> ------ remove read permission of user
chmod u-rx <filename>  ----------------- remove read and execute permission from user
chmod g+rwx <filename>   ----------------- add write permission for group
chmod o=rw <filename>  ----------------- assign permission of read and write for others (old permission will be removed)


r  =4
w  =2
x  =1   

chmod 777 file.txt 

-user  --7  (rwx)
-group --7  (rwx)   ------ rwxrwxrwx
-other --7  (rwx)

chmod 732 file.txt

user  --7  (rwx)
group --3  (wx)    ------ rwx-wx-w-
other --2   (w)

chmod 651 file.txt 

user --6  (rw)
group --5 (rx)  --------- rw-r-x--x
other --1 (x)


644, ---- rw-r--r--
731, ---- rwx-wx--x
512, ---- r-x--x-w-
335  ---- -wx-wx-r-x

Task: 
bydefault permissions for root user  ----- for file and directory  file- 644   dir- 755
bydefault permission for local user  ----- for file and directory  file- 664   dir- 775


#There are two types of symblolic link
1. Hard link
   - We create hard link for backup purpose
   - Hard links are not allowed for directories
   - it possible to create hard link of files only
   - it content actual data from original file
   - If the original file is removed, the link will still work as it accesses the data the original was having access to.
   - size is as actual as orginal file
   - Files that are hard linked take the same inode number.
   - command : ln <original_filename> <hardlink_name>

2. Soft link
   - Soft links can be used for linking directories
   - Soft links only point to the file name, it does not retain data of the file
   - If the original file is removed, the link will not work as it doesn’t access the original file’s data.
   - size of softlink depends on path of the file
   - Files that are soft linked take a different inode number.
   - command : ln -s <originalfile_name> <softlink_name>


Link count :
default link count of file - 1
default link count of directory - 2

-Link count of file will be change only when hardlink of it get created
-Linkcount of directory wiil be change when we create directory inside the directory


User and Group ownership :

chown <username> <filename/directory_name>    ------ change the ownaer of file or directory
chgrp <groupname> <filename/dir_name>    --------- chnage group ownership
chown <username>:<groupname> <file/dir_name>  ----- change owner and group owner


## Archive and Compression :

Archive -
   --- backup purpose
   --- tranfer the data in bundling format over the internet

tols -
  windows--- winRAR
  linux --- tar (tape archive)

command : 
   tar -cvf <archive_filename.tar> <file to be archive>
ex: tar -cvf etc.tar etc
   
   tar -tvf <archive_filename>  ------ for read the data
   tar -tvf etc.tar

   tar -xvf <archived_filename> ------- extract archive file
   tar -xvf etc.tar 
   tar -xvf etc.tar -C /root/  ------- extract file in different location

   du -sh <filename>    ------ to see size of file


   options: 
        -c ----- create
        -v ----- verbose/view
        -f ----- forcefully
        -x ----- extract

 Compression :
 1) gzip (z)
    command: gzip <archive_filename>
            gzip /etc.tar   ------------> etc.tar.gz
            gunzip etc.tar.gz   --------- unzip the compress file

 2) bzip2 (j)
   command: bzip2 /etc.tar -------------> etc.tar.bz2
            bunzip2 etc.tar.bz2 --------

 3) xz (J)
   command: xz /etc.tar ----------------> etc.tar.xz
            unxz etc.tar.xz

check the size of file :
 command : du -sh <file_name> 


archive and compression in single command :
 1. tar -czvf /etc.tar.gz /etc  -------- archive and compress using gzip
   tar -xzvf /etc.tar.gz -C /mnt/ ------ decompress and extract the file

 2. tar -cjvf /etc.tar.bz2 /etc -------- archive and compression using bzip2
    tar -xjvf /etc.tar.bz2 -C /home/ --- decompress and extract the file

 3. tar -cJvf /etc.tar.xz /etc --------- archive and compresiion using xz
    tar -cJvf /etc.tar.xz -C /root/ ---- decompress and extract the file

Login to your aws account
- search ec2 (elastic cloud compute)
- click on launch instamce
- give name to machine
- select os (ubuntu)
- create key pair 
- leave other settings as bydefault
- and click on launch instance

- wait for get the status check of instance 2/2
- then open windows terminal
- run command : cd .\Downloads\
- go to aws cansole select launched instance, then click on connect
- select their option ssh client
- copy the command, wich will be in example: tab
- paste it in windows terminal 
- you will be connect with your remote server


## Scheduling task :

Tools :
 1. at  (non-periodic task)
 2. crontab (periodic task)
 3. anacron (desktop server)

1) at :
 # apt update
 # apt install at

 command :
   at "15:20 23 dec 2024"  
   at> touch /file.txt
   at> mkdir /home/demo
   ctrl+D

   atq  --------- to show schedule jobs (at queue)
   at -c <job_id> ------ show more info about schedule task
   atrm <job_id> ------- to remove task

2) crontab
   /etc/crontab     ----------- crontab file

   *      *    *      *       *
   min   hr   date   month  day of week

   min (0-59)
   hr (0-23)
   date (1-31)
   month (1-12)
   day (0-6) (0 or 7= sunday)

   crontab -e     ------------- to schedule the cron jon
    * * * * *  <path_of_command> <operatio_to_be_performed>

    which <command> --------------- to find path of command
    which touch

   1. 15:59 
      59 15 * * *  /bin/touch /crontab.txt  -----> create crontab.txt inside "/" at 15:59 
   2. 10 sep 20:45
      45 20 10 sep *
   3. 7:00 am only on monday to friday
      0 7 * * mon-fri
   4. only on saturday at every minute
      * * * * sat
   5. evry 5 min
      */5 * * * *
   6. every 3 hr
      0 */3 * * *
   7. start from 06:08 and execute at every 5 min of interval
      8/5 6 * * * 


## Search and Filter utility in Linux :

1) sort <file_name>  --------- sorts the lines alphabetically
2) sort -r <file_name> -------sorts the lines alphabetically in reverse
3) uniq <filename>  --------- removes dupicate lines
4) wc <file_name> -------- shows numbers of lines, words, size of file
   wc -l <file_name>
   wc -w <file_name>
5) locate <file_name> --------- find path of file from database
   - apt update
   - apt install plocate -y

   - locate <file_name>
     updatedb --------------- manually update database

6) find   --------- find the file path with multiple options
   - find /root -name <file_name>
   - find / -perm 644
   - find / -size +100M
   - find / -user ubuntu

7) grep --------used to search perticular informsation from file
   - grep "Da" flower.txt

task: 1) find -------- find out multiple options use with find command
      2) egrep or grep -E
      3) '|' ---- pipe command vs "&&" command


## Process managemnt :
  
   Process : Running executable programs

   1. Shell jobs
   2. Daemon jobs ---- daemon process (system process)


   1. shell jobs  ------ run by users

      sleep 300 
      ctrl+d  ------- save the job
      ctrl+z  ------- stop the process
      cltrl+c ------- cancel the process

      sleep 700 & ----------- run the job in background

      jobs   --------------- list all stopped or running jobs

      bg %<job_ID> --------- run the job in background
      fg %<job_ID> -------- run the job in foreground 

   command :

   1. ps -elf
   2. ps -aux
   3. ps -el


      F       S     UID      PID     PPID      C   PRI  NI  ADDR SZ WCHAN  STIME TTY          TIME CMD
     flag  state user ID  ProcessId Parent_processID  


flag : 1 - running in memory, 4- running with supper user permission
state of process : R - running process
                   T - stopped process
                   S - sleeping process (waiting for an event to complete). INTERRRUPTABLE_SLEEP
                   D - process in sleep state that can not be stopped (UNINTERRUPTABLE_SLEEP)
                   Z = ZOMBIE

               D    uninterruptible sleep (usually IO)
               I    Idle kernel thread
               R    running or runnable (on run queue)
               S    interruptible sleep (waiting for an event to complete)
               T    stopped by job control signal
               t    stopped by debugger during the tracing
               W    paging (not valid since the 2.6.xx kernel)
               X    dead (should never be seen)
               Z    defunct ("zombie") process, terminated but not reaped by its parent

PRI : priority value
NI : NIce Value ------ range (-20 to 19)  lower the nice value get higher priority
     command to change nice value:
          renice -n <nice_nuber> -p <process_ID>
          renice -n -10 -p 1222

ADDR : memory address
SZ : size 
WCHAN : waiting chanel
STIME : process start time
TTY : terminal type

command :
 top 

  load average: 0.79,       1.46,       0.73
                (per min)  (per 5min)  (per 15 min)

   increase stress of server/cpu
   - apt update
   - apt install stress
   - stress -c 4

    command to kill the process ;
     1) kill <PID>
     2) kill -9 
     3) killall <command name>
        killall sleep -------------- kill all running process name with sleep
     4) pkill <command name>
        pkill sleep 

      kill the process in top 
       - press "k" key
       - provide the process id
       - enter 



Networking :

OSI mode

1> Application layer 
 protocol - http, https,ftp,smtp, DNS, telnet


 ip classes and its ranges


 Tpes of ip :
 IPv6 -- 128 bit

 IPv4 -- 32 bit -- 4 octets

 1 octes = 8 bit
 
 11111111         11111111         11111111       11111111
   255              255              255             255

1      1       1        1       1      1       1    1
2^7   2^6     2^5      2^4     2^3    2^2    2^1   2^0
128    64     32        16      8       4      2    1    = 255


0-255  0-255  0-255  0-255

0.0.0.0 - 255.255.255.255


Class A : 1.0.0.0   to  126.255.255.255
Class B : 128.0.0.0 to  191.255.255.255
Class C : 192.0.0.0 to  223.255.255.255
Class D : 224.0.0.0 to  239.255.255.255
Class E : 240.0.0.0 to  255.255.255.255

Public IP and Private IP : 



10.255.255.255 --- > 11.0.0.0
                     11.0.0.1
                     11.0.0.2
                          |
                     11.0.0.255
                     11.0.1.0
                     11.0.1.1
                     11.0.1.2
                         |
                     11.0.1.255
                     

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
mkdir /project ------- directory will be crreated inside the / directory
mkdir /project/demo ------- demo directory will be created inside practice dir.
mkdir -p /root/project/practice ---------- create parent directory 
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


Hierachy Of linux file system :
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

**Eitior in Linux 

In windows :- note pad, m. world, vs code

In Linux :- 
  *Graphical editior --- gedit, kedit

  *CLI editiors ------- pico, nano, vi, vim

  **vim editor 
    1) command mode
    2) Insert mode
    3) Execution mode
    4) Visual mode

    1) Command mode :
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

    2) Insert mode : 
       we can edit the data manually
       1. i ------- to inster into inser mode 
       2. I ------- inser text at start of the line
       3. a 
       4. A
       5. o 
       6. O  
       7. r  
       8. R ------ 

    3) Execution mode : 
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

    4) Visual mode :
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

Topic : Managing Users and Permissions in Linux :-

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

   Files get affect after useradd in the system
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
           
        1) usermod -u 2000 nikita     -------- for change the userid UID
        2) usermod -c "devops engineer" nikita ------- change the comment





   5. /etc/shadow 
       ----- user passowrd informaton

hemraj: $y$j9T$oXv8/KZclX2EUiYoREqfF.$9owMeytAiWkYKJQQP   :20073   :6  :90   :7 :20 :30 march 2025 :
            
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
   chage -l <username>  -------list the password onformation
   chage -m <username> ------ change minimum days between password change
   chage -M <username> ------- maximum password age
   chage -W <username> ------- warning days
   chage -I <username> ------- password inactive days
   chage -E <username> ------- account expired


  6. /etc/group  ------
        
  7. /etc/gshadow -----

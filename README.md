# Bandit Over The Wire

Download putty (windows) to SSH into Host: 

bandit.labs.overthewire.org / Port: 2220

![image](https://github.com/user-attachments/assets/f7075d11-a06a-4ab9-98e8-7bead3d906fc)



# Bandit 0

Username/ Password: bandit0

Hint: password is in a readme file.

Use < ls > to list down the files and folders

and use < cat readme > to read the content

    - key: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

![image](https://github.com/user-attachments/assets/728f4d89-52c4-491c-91ab-043c1d11c846)


< putty was annoying with logging in and exiting. moved to powershell from now... lol



# Bandit 1

ssh bandit1@bandit.labs.overthewire.org -p 2220

Hint: pasword is in a file called -

use < ls -la > to list all the files in the directory including the hidden files and the executables.

use < cat ./filename > to extract data from a file with a special character as a filename

    - key: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

![image](https://github.com/user-attachments/assets/f1cbd05f-3a9c-4036-b929-49daea379ba6)




# Bandit 2

ssh bandit2@bandit.labs.overthewire.org -p 2220

Hint: pasword is in a file called spaces in this filename

use < ls -la > to list all the files in the directory including the hidden files and the executables.

use < \ > character before the space to type out the filename

    - key: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

![image](https://github.com/user-attachments/assets/30376592-475d-4bbc-a258-0ca4f699d692)




# Bandit 3

ssh bandit3@bandit.labs.overthewire.org -p 2220

Hint: password is stored in a hidden file in the inhere directory

use < ls -la > to list all the files in the directory including the hidden files and the executables.

use < cd > go into inhere directory

use < \ > character before the space to type out the filename

    - key: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

![image](https://github.com/user-attachments/assets/6d82aa2b-6449-4404-85c2-0ddf1fdef4ca)




# Bandit 4

ssh bandit4@bandit.labs.overthewire.org -p 2220

Hint: password is stored in the only human-readable file

use < ls -la > to list all the files in the directory including the hidden files and the executables.

use < cd > go into inhere directory

use find -type f -exec file {} + | grep ASCII

1. < find -type f >  -  This searches for all files (-type f) in the current directory and its subdirectories.

2. < -exec file {} + >  -  The file command determines the type of each file.

  a. < -exec >  -  This tells find to run a command on each file it finds. 
  
  b. < file {} >  -  file is a tool that looks inside a file and tells you what kind of file it is.
 
  c. < {} > -  is a placeholder that gets replaced with each file found.
  
  d. < + >  -  instead of running file one by one for each file, this makes it run on multiple files at once (which is much faster).

3. < | grep ASCII >  -  Filters the output to only show lines containing "ASCII," meaning it will display only files that are identified as ASCII text.

        - key: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

![image](https://github.com/user-attachments/assets/9584af8e-0d2c-44ef-a5fc-2fd2353040b6)




# Bandit 5

ssh bandit5@bandit.labs.overthewire.org -p 2220

Hint: file somewhere under the inhere directory and has all of the following properties: human-readable, 1033 bytes in size, not executable

use < ls -la > to list all the files in the directory including the hidden files and the executables.

use < cd > go into inhere directory

use find -type f -exec file {} + | grep ASCII

1. < find -type f >  -  This searches for all files (-type f) in the current directory and its subdirectories.

2. < -size 1033c >  -  This finds files exactly 1033 bytes (c stands for "bytes").

3. < ! -executable >  -  This finds files that are not < ! > executables.

4. < -exec file {} + >  -  The file command determines the type of each file.

  a. < -exec >  -  This tells find to run a command on each file it finds. 
  
  b. < file {} >  -  file is a tool that looks inside a file and tells you what kind of file it is.
 
  c. < {} > -  is a placeholder that gets replaced with each file found.
  
  d. < + >  -  instead of running file one by one for each file, this makes it run on multiple files at once (which is much faster). 

4. < | grep ASCII >  -  Filters the output to only show lines containing "ASCII," meaning it will display only files that are identified as ASCII text.

        - key: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

![image](https://github.com/user-attachments/assets/ffc17343-f02d-477b-8670-adc831ad039f)



# Bandit 6

ssh bandit6@bandit.labs.overthewire.org -p 2220


has all of the following properties:

Hint: file somewhere in the server and has all of the following properties: owned by user bandit7, owned by group bandit6, 33 bytes in size



![image](https://github.com/user-attachments/assets/8a0a434b-183a-4b0d-88b5-ce13fb8685c2)





find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null









































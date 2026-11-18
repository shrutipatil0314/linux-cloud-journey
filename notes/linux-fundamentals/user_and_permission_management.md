*** user and permission managment ***

every file and directory in linux has specfific permissions restricting 
who can interact with it 


there are 3 type of permissins 

r --> read 

w --> write 

x --> execute = running a program 


Each permission (rwx) can be controoled at three levels 

u --> user = yourself 

g --> group = can be people in the same project

o --> other = everyone on the system 


Displayed by running ls -l command 

-         rwx      rwx      rwx

file     user     group    other


Command to change permissions

1. chomod ( change modifications )

2. Man chmod - manual menu on change mod contains all command 


Commands 

1. chmod g-w filename --> where 
   g = group w = write 

about command removes write permission from group in the file mentioned

2. chmod g + w filename --> same but adds permission 

3. chmod a-r-w-x filename --> will remove read permission from form  all at once

4. chomod a+r+w+x  filename --> will add all permission from all at once



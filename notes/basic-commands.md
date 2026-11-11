
**-BASIC COMMANDS -**
1. System information
uname -a = system and kernel info
pwd = enter pwd in your terminal to see where you are
whoami = if you forgotten whether your logged on as root or anther user
date = current date and time 
df -h = disk space
du -sh folder = size of a folder
free -h = memory usage
uptime = how long the system has been running
history = commands you typrd brfore 
clear = clear the screen

2. navigating the linux filesystem

cd = changing directories 
cd/etc
cd.. = to move up one level in file structure
cd~ = Go to your home folder
cd - = Go back to the previous folder
cd folder	Go into a folder

ls = listing the  contents of a directory 
ls - l = to get more information about the files and directories 
ls - a to show hidden files 
 
ls -la  =you can combine them into one 

3. Getting help 

--help = nearly every command application 
-h -? = you can use this to get help file 

4. Modifying Files and Directories

Creating file

cat = filename will display thecontents of that file but to create 
cat > = it create  file   
less = Scroll through a file (q to quit)
head = First 10 lines
tail = Last 10 lines
tail -f = Watch a file update live (great for logs)
nano = Edit a file
wc -l = Count lin

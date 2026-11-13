
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

cd logs = relative path

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

tail -20 = to displaying the last 20 lines 

n1 = displaying line numbers in terminal output 
nano = Edit a file

wc -l = Count lin

5. Searching 

grep "word" file = Find text inside a file

grep -r "word" . = Search all files in a folder

find . -name "*.txt" = Find files by name

which command = Show where a command lives

6. Files and folders

mkdir name = Create a folder

mkdir -p a/b/c	= Create nested folders

touch file.txt = Create an empty file

cp a.txt b.txt = Copy a file

cp -r dir1 dir2	= Copy a folder

mv old new = Move or rename


rm file.txt = Delete a file

rm -r folder = Delete a folder

rmdir folder = Delete an empty folder

7. Processes

ps aux = List running processes

top = Live process view (q to quit)

kill PID = Stop a process by its ID

systemctl status name = Check a service


8. Packages (Ubuntu)

sudo apt update = Refresh the package list

sudo apt upgrade = Update installed software

sudo apt install name = Install software

sudo apt remove name = Remove software

9. Networking

ping google.com	= Test a connection

curl url = Fetch a web page

ip a = Show your IP addresses

ssh user@host = Connect to another computer


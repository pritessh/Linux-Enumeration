# Linux Enumeration

### Distribution type and version of Operating System  
<ins>Command cat /etc/issue used for check version of operating system</ins>

### Identify Kernel Version  
<ins>Following commands are used for identify kernel version of Operating System</ins>

cat /proc/version  
uname -a  
uname -mrs

### Identify Environment Variables  
<ins>Following commands are used for identify environment variables</ins>
cat /etc/profile  
cat /etc/bashrc  
cat ~/.bash_profile  
cat ~/.bashrc  
cat ~/.bash_logout  
env  
set  

### Which services running and Which service has which user privilege in operating system  
<ins>Following commands are used for check running services and user privilege of services </ins>
ps aux  
ps -ef  
top  
cat /etc/services  

### Identify which application is installed with version of that application  
<ins>Following commands are used for identify which application and what is the version of application is installed</ins>  
ls -alh /usr/bin/  
ls -alh /sbin/  
dpkg -l  

### Identify User information and Sensitive Files
<ins>Following commands are used for identify user information and sensitive files</ins>  
id  
w  
last  
cat /etc/passwd | cut -d: -f1    # List of users  
grep -v -E "^#" /etc/passwd | awk -F: '$3 == 0 { print $1}'   # List of super users  
awk -F: '($3 == "0") {print}' /etc/passwd  

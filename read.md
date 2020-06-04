# Linux Enumeration

### 1. Distribution type and version of Operating System  
<ins>Following commands used for check version of operating system</ins> 

cat /etc/issue  
cat /etc/*-release  

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/1.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/2.JPG)

### 2. Identify Kernel Version  
<ins>Following commands are used for identify kernel version of Operating System</ins>

cat /proc/version  
uname -a  
uname -mrs

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/3.JPG)

### 3. Identify Environment Variables  
<ins>Following commands are used for identify environment variables</ins>  

cat /etc/profile  
cat /etc/bashrc  
cat ~/.bash_profile  
cat ~/.bashrc  
cat ~/.bash_logout  
env  
set  

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/4.JPG)

### 4. Which services running and Which service has which user privilege in operating system  
<ins>Following commands are used for check running services and user privilege of services </ins>

ps aux  
ps -ef  
top  
cat /etc/services  

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/5.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/6.JPG)

### 5. Identify which application is installed with version of that application  
<ins>Following commands are used for identify which application and what is the version of application is installed</ins>  
ls -alh /usr/bin/  
ls -alh /sbin/  
dpkg -l  

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/7.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/8.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/9.JPG)

### 6. Identify User information and Sensitive Files
<ins>Following commands are used for identify user information and sensitive files</ins>  
id  
w  
last  
cat /etc/passwd | cut -d: -f1    # List of users  
grep -v -E "^#" /etc/passwd | awk -F: '$3 == 0 { print $1}'   # List of super users  
awk -F: '($3 == "0") {print}' /etc/passwd  

![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/10.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/11.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/12.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/13.JPG)
![](https://github.com/pritessh/Linux-Enumeration/blob/master/images/14.JPG)

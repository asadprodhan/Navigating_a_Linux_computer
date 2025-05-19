<h1 align="center">Navigating a Linux Computer</h1>

<h3 align="center">Asad Prodhan<sup>*</sup></h3>


<div align="center"><b> DPIRD Diagnostics and Laboratory Services </b></div>


<div align="center"><b> Department of Primary Industries and Regional Development </b></div>


<div align="center"><b> 3 Baron-Hay Court, South Perth, WA 6151, Australia </b></div>


<div align="center"><b> <sup>*</sup>Correspondence: Asad.Prodhan@dpird.wa.gov.au </b></div>


<br />


<p align="center">
  <a href="https://github.com/asadprodhan/sangerFlow#GPL-3.0-1-ov-file"><img src="https://img.shields.io/badge/License-GPL%203.0-yellow.svg" alt="License GPL 3.0" style="display: inline-block;"></a>
  <a href="https://orcid.org/0000-0002-1320-3486"><img src="https://img.shields.io/badge/ORCID-green?style=flat-square&logo=ORCID&logoColor=white" alt="ORCID" style="display: inline-block;"></a>
</p>


<br />


### **Q: How to use my Linux computer remotely?**


- Open a ssh client. For example, MobaXterm
- Click on ‘Session’ located at top-left corner
- Fill up the following boxes and click ‘OK’:
	- Remote host
  	- Specify username
  	- SSH-browser type as SFTP protocol


<br />


<p align="center">
  <img 
    src="https://github.com/asadprodhan/Navigating_a_Linux_computer/blob/main/MobaXterm.png"
 align="center" width=60% height=60% >   
</p>
<p align = center>
Figure 1: MobaXterm.
</p>


<br />


### **Q: How to enable sftp on the sidebar in the MobaXterm?**


- Go to MobaXterm Session settings > SSH > Fill up Remote host > Specify username > Select ‘SFTP protocol’ from the ‘SSH-browser type’ drop down menu 

<br />

### **Q: How to transfer data between a remote computer and your local laptop?**


Option 1: Drag and drop using the left panel of your MobaXterm


Option 2: sftp
- sftp username@remote_host:/destination_directory 
- ‘put -r’ to transfer data from local to remote
- ‘put -ar’ to transfer data that failed in the first attempt
- ‘get -r’ to transfer from remote to local


<br />


# 🐧 Linux Usage Exercise for New User

Welcome to Linux training! This brief guide will help you get started with essential Linux commands and concepts.

<br />


### 📁 1. Working with Directories (i.e. Folders)

Check your current location

```
pwd
```

See what you have in your current location

```
ls
```

Create a new directory called 'practice'

```
mkdir practice
```

Move into the directory

```
cd practice
```

Create nested directories

```
mkdir -p projects/scripts
```

Go up one directory

```
cd ..
```

<br />


### 📄 2. Working with Files

Create a new text file

```
echo "Hello, Linux!" > hello.txt
```

View the content

```
cat hello.txt
```

Copy the file

```
cp hello.txt hello_backup.txt
```

Rename the file

```
mv hello.txt greetings.txt
```

Delete the backup

```
rm hello_backup.txt
```

<br />


### 🔍 3. Viewing and Searching


View contents of a file

```
less greetings.txt
```

Search inside the file

```
grep "Hello" greetings.txt
```

List files with details

```
ls -lh
```


<br />


### 👥 4. User and Permissions


Check who you are

```
whoami
```

See your groups

```
groups
```

Check file permissions

```
ls -l greetings.txt
```

Change permissions (read/write for user only)

```
chmod +x greetings.txt
```

Or,

```
chmod +x *
```

<br />


### ⚙️ 5. System Information and Help


View disk usage

```
df -h
```

See memory usage

```
free -h
```

View running processes


```
top
```

Get help on commands


```
man ls
```

<br />


### 🧑‍💻 6. Sudo and Package Installation


Update package list 

```
sudo apt update
```

Install a basic tool (example: tree)


```
sudo apt install tree
```

Use the installed tool


```
tree
```

<br />


### ✅ 7. Create a Simple Script


Create a script file

```
nano say_hello.sh
```

Paste the following content into the file:


```
#!/bin/bash
echo "Hello, $USER! Today is $(date)."
```

Then run:


Make it executable

```
chmod +x say_hello.sh
```

Execute the script


```
./say_hello.sh
```


<br />


### 🚀 You're Ready!

You've just taken your first steps into Linux! Continue experimenting using the following Linux commands to explore further


<br />


## **GREP**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| grep | Search and print lines containing a word | grep 'salmon' File.tsv > FileSalmon.tsv |
| grep --color | Search text | grep --color "Lunch" File1.txt |
| grep --color -A 2 "word" | Print 2 lines after the match |	grep --color -A 2 "word" File1.txt |
| grep --color -B 2 "word" | Print 2 lines before the match | grep --color -B 2 "word" File1.txt |
| grep --color -C 2 "word" | Print 2 lines before and after the match | grep --color -C 2 "word" File1.txt |
| grep -v "word" | Find everything except 'word' | grep -v "word" File1.txt |
| grep -c "[WW]ord" | Count the occurrence of 'W/word' | grep -c "[WW]ord" File1.txt |


<br />

## **SED**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| sed -n 3p |	Extract the 3rd line | sed -n 3p File1.txt |
| sed -n 3-5p | Extract the 3rd to 5th lines | sed -n 3-5p File1.txt |
| sed 's/Find/Replace/g' File.txt | Find and replace | sed 's/Ishmael/Dave/g' File1.txt; "Ishmael" replaced by "Dave" |
                                                      

<br />


## **AWK**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| awk '{print $1,$2,$3,$4,$5,$7}' | Subset columns 1-5, 7 | awk '{print $1,$2,$3,$4,$5,$7}' file.tsv	
| awk '{print $3}' | Print third column | awk '{print $3}' File.tsv |
| awk '{print $3,"\t"50}' | Print third column and add 50 at reach row; /t is tab space | awk '{print $3,"\t"50}' File.tsv | 
| awk '{print $3,"\t"$3+1}' | Print third column and add 1 with all row values | awk '{print $3,"\t"$3+1}' File.tsv | 


<br />

## **CUT**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| cut -f1,2,3,4,5,7 | Subset columns 1-5, 7 | cut -f1,2,3,4,5,7 File1.txt	

<br />

## **NANO**


| Code/Symbol	| Function/Example |	
|:----------|:----------|
| alt+sht+$	| wraps lines |
| alt+sht+y	| highlights syntex |
| alt+sht+#	| puts line number |
| fg | to return to nano |
| ctrl+K | deletes entire line |
| ctrl+A | moves the cursor at the beginning of the line |
| ctrl+E or Alt+/ | moves the cursor at the end of the line |
| Ctrl+Shift+- 7406148 | Jump to line number 7406148 |
| Ctrl+W | Search for words |

<br />

## **PUTTY**


| Code/Symbol	| Function/Example |	
|:----------|:----------|
| psftp> get -r * | download one file |
| psftp> mget -r * | download multiple files |
| psftp> put -r * | upload one file |
| psftp> mput -r * | upload multiple files |
	

<br />

 ## **TMUX**


| Code/Symbol            | Function/Example |	
|:----------             |:----------|
| tmux > press enter     | start tmux session |
| Ctrl-b d               | detach from the tmux session but the session will continue running in the background |
| tmux list              | list all the active tmux sessions. Left-hand column shows the session numbers |
| tmux attach -t 1       | logging in into tmux session 1 |
| tmux kill-session -t 1 | terminating tmux session 1 | 


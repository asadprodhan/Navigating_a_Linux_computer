# **Navigating a Linux computer** <br />


### **AUTHOR: Dr Asad Prodhan** https://asadprodhan.github.io/
<br />


## **GREP**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| grep --color | Search text | grep --color "Lunch" File1.txt |
| grep --color -A 2 "word" | Print 2 lines after the match |	grep --color -A 2 "word" File1.txt |
| grep --color -B 2 "word" | Print 2 lines before the match | grep --color -B 2 "word" File1.txt |
| grep --color -C 2 "word" | Print 2 lines before and after the match | grep --color -C 2 "word" File1.txt |
| grep -v "word" | Find everything except 'word' | grep -v "word" File1.txt |
| grep -c "[WW]ord" | Count the occurrence of 'W/word' | grep -c "[WW]ord" File1.txt |


## **SED**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| sed -n 3p |	Extract the 3rd line | sed -n 3p File1.txt |
| sed -n 3-5p | Extract the 3rd to 5th lines | sed -n 3-5p File1.txt |
| sed 's/Find/Replace/g' File.txt | Find and replace | sed 's/Ishmael/Dave/g' File1.txt; "Ishmael" replaced by "Dave" |
                                                      

## **AWK**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| awk '{print $1,$2,$3,$4,$5,$7}' | Subset columns 1-5, 7 | awk '{print $1,$2,$3,$4,$5,$7}' file.tsv	
| awk '{print $3}' | Print third column | awk '{print $3}' File.tsv |
| awk '{print $3,"\t"50}' | Print third column and add 50 at reach row; /t is tab space | awk '{print $3,"\t"50}' File.tsv | 
| awk '{print $3,"\t"$3+1}' | Print third column and add 1 with all row values | awk '{print $3,"\t"$3+1}' File.tsv | 


## **CUT**


| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|:----------|:----------|:----------|
| cut -f1,2,3,4,5,7 | Subset columns 1-5, 7 | cut -f1,2,3,4,5,7 File1.txt	


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


## **PUTTY**


| Code/Symbol	| Function/Example |	
|:----------|:----------|
| psftp> get -r * | download one file |
| psftp> mget -r * | download multiple files |
| psftp> put -r * | upload one file |
| psftp> mput -r * | upload multiple files |
	

 ## **TMUX**


| Code/Symbol            | Function/Example |	
|:----------             |:----------|
| tmux > press enter     | start tmux session |
| Ctrl-b d               | detach from the tmux session but the session will continue running in the background |
| tmux list              | list all the active tmux sessions. Left-hand column shows the session numbers |
| tmux attach -t 1       | logging in into tmux session 1 |
| tmux kill-session -t 1 | terminating tmux session 1 | 


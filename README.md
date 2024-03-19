# Navigating a Linux computer


### GREP



| Code/ Symbol	| Command/ Elaboration |	Function/ Example |
|----------:|:----------|:----------|
| grep --color | Search text | grep --color "Lunch" File1.txt |
| grep --color -A 2 "word" | Print 2 lines after the match |	grep --color -A 2 "word" File1.txt |
| grep --color -B 2 "word" | Print 2 lines before the match | grep --color -B 2 "word" File1.txt |
| grep --color -C 2 "word" | Print 2 lines before and after the match | grep --color -C 2 "word" File1.txt |
| grep -v "word" | Find everything except 'word' | grep -v "word" File1.txt |
| grep -c "[WW]ord" | Count the occurrence of 'W/word' | grep -c "[WW]ord" File1.txt |

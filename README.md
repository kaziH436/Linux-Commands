# Linux-Commands
linux commands for data science 


## Env Variables
A variable across all shell sessions 

## Shell Variables
A variable only in that one shell sessions and destroyed when the terminal is terminated 

## Common Commands
- cd: change directory
- mkdir: make directory 
- remove recursive: rm -r <filename>
- mv <filename>.zip <file_path>
- pwd: print working dir 
- unzip <filename>
- && || 
- ls: lists all file
- copy a file: cp <optional: filepath>/<filename>.(extension maybe csv) <newfilename>.(extension).
  - the file path depends on where the current dir is so find it out using `pwd`
- -v: verbous

## Data Cleaning commands 
- to find the number of rows: wc -l <filename>.csv
   - the wc: word count and -l means line
  - wc alone gives the number of bytes (characters), number of words and number of lines
- wildcard: wc -l *.csv
- head -n 5 <filename>.csv gives the first 5 rows of csv
- cut means only take the chaacters selected: cut -c 1,3,4 <filename>.csv
  - in this case, only take the first, third and fourth, (index starts from 1 not 0)
  - range like this 1-9 is possible
      - 1- and -9 is possible

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
- taking a sample of rows and putting it in a new file: head n 7 <filename>.csv > <newfilename>.csv
- append to the new file name: tail -n 3 <filename>.csv >> <filename>.csv
- f: columns number and d: delimiter (comma, tabs: default) `cut -d , -f,2 <filename>.csv
  - -f,2,3,4
- sort: numbers before letter
  - if letters are same so like fish and fan, the order is fish, fan
  - capital comes before small letter
  - the order is then followed as is
  - sort -r: reverse sort
  - `u`: unique (removes duplicate rows) not sure what its comparing
  - 'k': sort by a specific column
  - 'n': sort numerically in increasing order
  - cut -d, -f 1-3 onlineretail.csv | sort -k3n -t | tail -n 10
- uniq (only removed duplicate when adjacent to each other so the csv needs to be sorted)


## Excersize
### How many lines are duplicates are there?
val1=$(cat Onlineretal.csv | wc -1)
val2=$(cat Onlineretal.csv | sort | uniq| wc -1)
echo "$((val1-val2))"

### Value counts in linux commands 
cut -d , -f 3 OnlineRetail.csv | sort | uniq -c | sort -rn | head -n 20



# Lab Report 3

## Find command

### '-type'

This command allows you to search for files based on their type.\
Example 1: Find all regular files in the technical directory.
~~~
find ./technical -type f
~~~
Output:
~~~
./technical/biomed/1471-2334-3-9.txt
./technical/biomed/1471-2350-2-11.txt
./technical/biomed/1471-2350-2-12.txt
./technical/biomed/1471-2350-2-2.txt
./technical/biomed/1471-2350-2-8.txt
./technical/biomed/1471-2350-3-1.txt
./technical/biomed/1471-2350-3-12.txt
./technical/biomed/1471-2350-3-7.txt
./technical/biomed/1471-2350-3-9.txt
...
~~~
*Found 1014 files only listing the first couple*\
Example 2: Find all the directories in the technical directory.
~~~
find ./technical -type d
~~~
Output:
~~~
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
~~~
[Source](https://www.gnu.org/software/findutils/manual/html_node/find_html/Type.html)

### '-name'

This command allows you to search for files by their names or patterns.\
Example 1: Find all files with "pmed" in the technical directory.
~~~
find ./technical -name "pmed*"
~~~
Output:
~~~
./technical/plos/pmed.0010008.txt
./technical/plos/pmed.0010010.txt
./technical/plos/pmed.0010013.txt
./technical/plos/pmed.0010021.txt
./technical/plos/pmed.0010022.txt
./technical/plos/pmed.0010023.txt
./technical/plos/pmed.0010024.txt
./technical/plos/pmed.0010025.txt
./technical/plos/pmed.0010026.txt
./technical/plos/pmed.0010028.txt
...
~~~
*Found 150+ files just listing the first couple*\
Example 2: Find all files starting with the letter "f" in the technical directory
~~~
find ./technical -name "f*"
~~~
Output:
~~~
./technical/government/Env_Prot_Agen/final.txt
./technical/government/Gen_Account_Office/ffm.txt
./technical/government/Media/families_saved.txt
./technical/government/Media/fight_domestic_abuse.txt
~~~
[Source](https://www.gnu.org/software/findutils/manual/html_node/find_html/Base-Name-Patterns.html)

### '-size'

This command allows you to search for files based on their size.\
Example 1: Find all files larger than 150KB(kilobytes) in the technical directory.
~~~
find ./technical -size +150k
~~~
Output:
~~~
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-3.txt
./technical/government/About_LSC/commission_report.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/government/Gen_Account_Office/pe1019.txt
~~~
Example 2: Find all files smaller than 2KB in the technical directory
~~~
find ./technical -size -2k
~~~
Output:
~~~
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
~~~~
[Source](https://www.gnu.org/software/findutils/manual/html_node/find_html/Size.html)

### '-empty'

This command allows you to search for empty files or directories.\
Example 1: Find all empty files in the technical directory.
~~~
find ./technical -type f -empty
~~~
Output:
~~~

~~~
*(None of the files are empty)*\
Example 2: Find all the empty directories in the technical directory.
~~~
find ./technical -type d -empty
~~~
Output:
~~~

~~~
*(None of the directories are empty)*\
Despite this command not really doing anything in this case because nothing is empty, I felt like it was a very useful command to include. \
[Source](https://lowendspirit.com/discussion/3930/howto-locate-empty-files-and-directories#:~:text=The%20command%20we%20are%20going,%20or%20files%20(f).)


# Shell Data Processing

  

  

### Background

[Hippocrates](https://en.wikipedia.org/wiki/Hippocrates) was a Greek physician. In the book [Airs, Waters and Places](http://classics.mit.edu/Hippocrates/airwatpl.mb.txt), Hippocrates has attempted to set forth a causal relationship between human diseases and the environment. I thought it would be interesting to know what were the most used words in this book so I attempted to find out.

---

  

### Commands

  

-  **curl** : Curl command is used here to retrieve all the contents of a web page. For example, ```curl http://classics.mit.edu/Hippocrates/airwatpl.mb.txt``` will get all the contents of this page.

  

-  **-O flag** : This flag will save to a file. For example, ```curl http://classics.mit.edu/Hippocrates/airwatpl.mb.txt -O data.txt``` will save texts retrived from ```curl http://classics.mit.edu/Hippocrates/airwatpl.mb.txt``` to data.txt.

  

-  **tr command** : This command will transform one text to other. Example, ```tr ' ' '\12'``` will transform space " " into ascii code \12 which is new line.

  

-  **Redirection (<)** : This will take input from a file. For example, ```tr ' ' '\12' < data.txt``` will take input from the file data.txt and will feed to ```tr ' ' '\12'```.

  

-  **Pipe ( | )** : This command will send the results of one command as input into another command. For example, ```tr ' ' '\12' < data.txt | sort``` will take input from ```tr ' ' '\12' < data.txt``` and pass it to sort command.

  

-  **Sort** : This command will sort the values in increasing order. For example, ```tr ' ' '\12' < data.txt | sort``` will take input from ```tr ' ' '\12' < data.txt``` and sort them in increasing order.

  

-  **uniq** : This command will filter out the repeated lines in a file. For example, ```tr ' ' '\12' < data.txt | sort | uniq``` will filter the repeated lines from the input passed from ```tr ' ' '\12' < data.txt | sort```.

  

-  **-c flag** : This flag is for counting. For example, ```tr ' ' '\12' < data.txt | sort | uniq - c``` will count all the repeated words that came from ```tr ' ' '\12' < returnedfile | sort | uniq```.

  

-  **-n flag** : This flag is used with sort and is used to compare according to string numerical value.

  

-  **-r flag** : This flag is also used with sort and is used to denote sorting in reverse order. i.e. if the sort is done in ascending order, using -r will do the sorting in decending order.

  

-  **Redirect Standard Output (>)** : This command is used to write/ redirect output to a new file. For example, ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt``` will redirect the output to a new file called result.txt.

  

---

  

### Tips:

  

If you want to go to the previous commands, hit up arrow key in the keyboard.
---
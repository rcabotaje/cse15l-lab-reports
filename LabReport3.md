# Lab Report 3

**grep-i** 

I found this command-line option using ChatGPT by typing "grep command-line options." It gave me a list of them I I chose this one because it looked
interesting.

The `grep -i` inline command is useful beacuse it will help you look for a specific word in a file. It works by after the `grep -i` is typed in the quotaion
marks is the word or phrase you're trying to find, and after that you can type the path to the file, or the file itself if you are in it's working
directory. It looks in each line of the file you're searching through and if it contians what's in the quotation mark it outputs all the lines that
contains whats in the quotation marks.

Ex1:
```
rommelcabotaje@Rommels-MBP stringsearch-data % grep -i "long" /Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/biomed/1468-6708-3-3.txt
        Without longer clinical follow up, it is not possible to
        coronary syndrome: First, the long-term safety and
        promote greater long-term utilization of these agents [ 18
```

Ex2:
```
rommelcabotaje@Rommels-MBP biomed % grep -i "chronic" 1468-6708-3-7.txt
          initiation, lasted during 5 to 6 months of chronic
          changes were followed by chronic sodium homeostasis and
          chronic congestive heart failure from a variety of these
        changes during chronic therapy. The long-term ramifications
        injury, or both. Chronic volume loading may not only unmask
```
---

**grep -v**

I found this command-line option using ChatGPT by typing "grep command-line options." It gave me a list of them I I chose this one because it looked
interesting.

The `grep -v` commad is useful because it lets you find lines in a file that doesn't contain a specific word/phrase. It works by after typing `grep -v`
whatever is in the quotation marks you put after is what to not include in its output, so when it searches thorugh the file you give, if a line in the file
contains whatever is in the quotation mark, its not outputted when the command is called. After the quotation marks you enter the path or file you want to 
search in.

Ex1:
```
rommelcabotaje@Rommels-MBP biomed % grep -v "a" 1468-6708-3-7.txt        
        Methods
      
      
        Results
        
        
        
        
        
          it does not lower high levels of endothelin-1 while
        
        
          findings.
        
      
      
        Conclusions
        this 2 to 3 mmHg difference in systolic blood pressure is
      
      
        Competing Interests
        by Wyeth Ay erst.
```
```
rommelcabotaje@Rommels-MBP technical % grep -v "e" /Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/biomed/1468-6708-3-7.txt

  
    
      
        Background
      
      
      
      
        
        
        
          kilograms.
          arms.
        
        
        
        
          findings.
        
      
      
        Conclusions
```
---

**grep -n**

II found this command-line option using ChatGPT by typing "grep command-line options." It gave me a list of them I I chose this one because it looked
interesting.

The `grep -n` command is useful because not only does it print the lines with the word/phrase you're trying to find, it also outputs the line it's on.
It works just the same as `grep -i` , just instead of an `-i` it uses `-n`. After typing `grep -n` you type in quotation marks what you're trying to find, 
then the path or file you want to search in. It looks inside the path/file and outputs the lines that has whatevers in the quotation marks, and its line
number.

Ex1:
```
rommelcabotaje@Rommels-MBP biomed % grep -n "1" 1468-6708-3-3.txt
6:        Three published [ 1 2 3 ] and one recently presented [ 4
35:        myocardial infarction and randomized them to 16 weeks of
51:        was 124 mg/dL. Atorvastatin treatment was associated with a
53:        (14.8% vs. 17.4%; RR relative risk [RR] 0.84, 95%
54:        confidence interval [CI] 0.70-1.00, p = 0.048). This
64:        fatal or non-fatal stroke by 0.8% (0.8% vs. 1.6%; RR 0.50,
68:        density lipoprotein (HDL) cholesterol by 16 weeks. By 16
70:        mg/dL in atorvastatin-treated patients but increased to 135
76:        placebo-treated patients (p < 0.001).
87:        identify a short-term (ie, within 16 weeks) clinical
129:        was realized after only 16 weeks of statin therapy, the
136:        of effect on these important endpoints at 16 weeks.
152:        revascularization [ 9 10 11 ] . Furthermore, a number of
155:        an early invasive strategy is applied [ 12 13 14 ] and it
173:        quite low (1.1%). Such therapy appears to be cost effective
174:        [ 15 16 ] , especially among high risk patients and is
176:        Cardiology/American Heart Association guidelines [ 17 ] .
204:        well-established [ 1 2 3 ] ; Second, as evidenced by
208:        promote greater long-term utilization of these agents [ 18
209:        19 20 21 ] . Finally, although lipid levels may be
254:        within 10 days of an acute coronary syndrome and
257:        over at least 1.5 years for the occurrence of myocardial
```
Ex2:

```
rommelcabotaje@Rommels-MBP biomed % grep -n "20" /Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/biomed/1468-6708-3-3.txt
209:        19 20 21 ] . Finally, although lipid levels may be
265:        In 2002, many would consider it unethical to withhold
```
--
**grep -l**

I found this command-line option using ChatGPT by typing "grep command-line options." It gave me a list of them I I chose this one because it looked
interesting.

The `grep -l` command is useful because it allows you to search multiple files to see if it contains a specific word/ phrase and outputs the files
that contian what you're looking for. It works by after typing `grep -l` you type in quotation marks what phrase/ word you're trying to find, then
the path and what type of file you want to search in. For example the `*.txt` searches any file that ends with a `.txt` in its path. Also if you use a 
type a path, then a `*.txt` it returns the paths to the files that have what's in the quotation marks, compared to jut typing `*.txt` when already 
inside the directory you want to look in, you just get the files.

Ex1:
```
rommelcabotaje@Rommels-MBP government % grep -l "problems" /Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/government/Alcohol_Problems/*.txt
/Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/government/Alcohol_Problems/DraftRecom-PDF.txt
/Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/government/Alcohol_Problems/Session2-PDF.txt
/Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/government/Alcohol_Problems/Session3-PDF.txt
/Users/rommelcabotaje/Documents/GitHub/stringsearch-data/technical/government/Alcohol_Problems/Session4-PDF.txt
```
Ex2:
```
rommelcabotaje@Rommels-MBP Alcohol_Problems % grep -l "problems" *.txt                                                                                               
DraftRecom-PDF.txt
Session2-PDF.txt
Session3-PDF.txt
Session4-PDF.txt
```

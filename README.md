# Problem Set 3
You should feel comfortable with GitHub by now. If you're not, come to office hours with me or the TAs.

If you think you see an error or typo, let me know! I will send out an email and post an announcement about any typos or errors you fine.

The deliverables for this problem set are the following:

* `ps3-part1.py`
* `ps3-part2.py`

**Remember** The sample code is your friend!

**Remember** I now expect you to write comments in your code! One point will be deducted if you do not provide comments explaining your code. Here's what I would like commented this time:

* Before every function you define, describe what it does and what its arguments are. Exception: you do not need to explain what `main()` is for.
* Before every variable you declare, explain what value it is holding. Exception: variables that appear after the keyword `for`.

**Remember** Now at the top of very files, you will include your honor pledge. The first four lines (comments) of every Python file should be this information. You will lose one point if you don't include these four lines.

* The name of the file.
* Your name.
* The date.
* "This code is my own work. I did not share my code or look at the code of another student. I did not consult ChatGPT, CoPilot, or another large language model."

**Note** You may not import any libraries to complete this assignment. IYKYK.

## Part 1: Counting words in a file
In this program you will read in a file, compile some statistics about the file, report those statistics to the user, and let the user ask about the frequencies of words and letters.

1. Write a function called `get_counts(filename)` that does the following:
   * Create an empty dictionary to store word counts called `word_counts`
   * Create an empty dictionary to store character counts called `char_counts`
   * Open the file and read the whole file into a string at once.
   * Split the string into a list of words using `split()`.
   * Go through that list of words, and use the `word_counts` dictionary to keep track of how many time you see each word.
   * Split the string into a list of characters using `list()`.
   * Go through that list of characters, and use the `char_counts` dictionary to keep track of how many time you see each character.
   * Return the following as a tuple: `word_counts` and `char_counts`.
  
2. Write a `main()` function that does the following:
   * Ask the user to supply a file name. Remember that whatever file you want to read must be in the same directory as your program! I have supplied a file in this repo called `testfile.txt`. You can just use that.
   * Call `get_counts()` passing in the user's chosen file name as the argument. Remember when you call the function you need to save out what it returns as a variable. It will return the words counts and the char counts, so you'll need to call the function like this:

```
wc, cc = get_counts(thefilename)
```
  * Report back to the user the total number of words, the total number of characters, the total number of unique words, and the total number of unique characters. You can use the `keys()` and `values()` functions to get this information from your dictinoaries.
  * Then ask the user what word they want to know the count of, and report back that count (or 0 if the word is not in the dictionary).
  * Then ask the user what character they want to know the count of, and report back that count (or 0 if the character is not in the dictionary).

3. Call `main()` by typing `main()` at the end of the file.

**MAKING INPUT LOOK NICE** When you use `input()`, it doesn't automatically insert a space before what the user enters. You don't want the user entering a space themselves, so you have to put the space at the very end of whatever you put in quotes as the argument to `input()`.

Here is some sample output using the file `testfile.txt`. Your output should be formatted exactly like this and have the same wording.

```
Enter a file to process: testfile.txt
This file has 532 words.
This file has 3126 characters.
This file has 284 unique words.
This file has 60 unique characters.
What word count would you like to look up? the
The count of "the" is 37.
What character count would you like to look up? e
The count of "e" is 308.
```

## Part 2: Word game word generator

Ask the user to provide a word with at least 4 but not more than 6 letters. If they enter a word with fewer than 4 characters or more than 6 characters, ask them to enter the word again and again until they get it right. Use a `while` loop.

Once you have their word, you will generate every possible four-letter word with no duplicate letters using the letters from the user's input word. After printing out all the possible "words", you will report the total number of words you generated. You should solve this problem using nested `for` loops and the `set()` function. You do not need to write any functions of your own.

Here is some sample output. Your output should be formatted exactly like this and have the same wording.
```
Enter a word that has at least 4 and no more than 6 letters: bee
Enter a word that has at least 4 and no more than 6 letters: elephant
Enter a word that has at least 4 and no more than 6 letters: tree
You entered tree.
I created 0 four letter words that contained no duplicate letters.
```

```
Enter a word that has at least 4 and no more than 6 letters: me
Enter a word that has at least 4 and no more than 6 letters: fireplace
Enter a word that has at least 4 and no more than 6 letters: smile
mesi mesl meis meil mels meli msei msel msie msil msle msli mies miel mise misl mile mils mles mlei mlse mlsi mlie mlis emsi emsl emis emil emls emli esmi esml esim esil eslm esli eims eiml eism eisl eilm eils elms elmi elsm elsi elim elis smei smel smie smil smle smli semi seml seim seil selm seli sime siml siem siel silm sile slme slmi slem slei slim slie imes imel imse imsl imle imls iems ieml iesm iesl ielm iels isme isml isem isel islm isle ilme ilms ilem iles ilsm ilse lmes lmei lmse lmsi lmie lmis lems lemi lesm lesi leim leis lsme lsmi lsem lsei lsim lsie lime lims liem lies lism lise
You entered smile.
I created 120 four letter words that contained no duplicate letters.
```

```
Enter a word that has at least 4 and no more than 6 letters: smell
mesl mels msel msle mles mlse emsl emls esml eslm elms elsm smel smle seml selm slme slem lmes lmse lems lesm lsme lsem
You entered smell.
I created 24 four letter words that contained no duplicate letters.
```

---

## Deadline: Wednesday, September 24, 2025, at 11:59pm EDT

## Deliverables

1. `ps3-part1.py` (Part 1: File Statistics)
2. `ps3-part2.py` (Part 2: Word Generator)

## Reminder: Important Guidelines
* Points will be deducted if your output does not match the required format.
* Points will be deducted if your files are not named as required.
* Points will be deducted if your files are not in the correct location (i.e., in the top-level directory where you see the `README`.)
* Points will be deducted if you do not include comments as desribed above.
* Points will be deducted if you do not include your honor pledge at the top of each file.




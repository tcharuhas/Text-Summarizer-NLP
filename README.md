# Text Summarizer - NLP
![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)

***So, how do I run this thing??***

Easy!  First, install Java on your machine.  Then all you need to do is head to the main function and make an object Summarizer, then call function Summarize.

    Summarizer test = new Summarizer();
    test.Summarize("your text/article here", desired amount of lines here); 
Then run

    javac //location of file
    java Summarizer
In the terminal


***Here's how this darn thing works***

 1. It starts by recording frequencies of words within the text; a Map works best for this
 2. Stopwords ("but","also", "is", etc) are filtered an removed; the goal being to reduce redundancy
 3. The Map is then sorted from greatest word frequency to least
 4. The sentences from your original text are formatted as to make sure any abbreviations/suffixes are not counted as the ending of a sentence
 5. For text that is from online, we need to format and adjust it so un-needed text is removed
 6. Finally, obtain the summary by going through the listof sentences and then using our Map to compare and find the key phrases and words from each sentence.  If found, add that sentence to the summary list
 7. Return the summary as a String

**Future Plans...**

-Eventually, I would like to touch up on the algorithm to make it summarize more accurately, but this was just my first dabble into NLP-type stuff

-Also, I may at some point integrate this into a web-app, but we will see...

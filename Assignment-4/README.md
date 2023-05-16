# Autocorrect Feature
## Data Used:
Moby-Dick; or, The Whale is a novel by Herman Melville, first published in 1851. It tells the story of the obsessive quest of Ahab, captain of the
whaling ship Pequod, for revenge on Moby Dick, a giant white whale that on a previous voyage destroyed his ship and severed his leg at the knee. </br>

The novel is considered to be one of the greatest works of American literature. It is a complex and challenging work, full of symbolism and allegory.
Moby-Dick has been interpreted in many different ways, but it is generally seen as a meditation on the nature of good and evil, the meaning of life,
and the limits of human knowledge.</br>

The text data in Moby-Dick is vast and varied. It includes whaling lore, descriptions of the natural world, and philosophical and theological musings.
Melville's writing is often lyrical and poetic, and he uses a wide range of literary devices, including symbolism, allegory, and allusion.</br>

Because this novel is a **large text corpus** with **diverse language usage** and **complex narrative and themes**, I found this to be suitable data.
</br>

## About Project
### Auto Correct:
Autocorrect is a feature in many software applications that automatically corrects spelling errors. It is helpful because it can help users to avoid
making mistakes and to communicate more effectively. Autocorrect is a classic application of natural language processing (NLP). NLP is a field of
computer science that deals with the interaction between computers and human (natural) languages. Autocorrect uses NLP techniques to identify
misspellings and to suggest corrections. </br>

There are two main types of autocorrect: </br>
- **Rule-based autocorrect**: This type of autocorrect uses a set of rules to identify misspellings. For example, a rule might state that "teh"
should be corrected to "the".
- **Statistical autocorrect**: This type of autocorrect uses statistical methods to identify misspellings. For example, a statistical autocorrect
might look at the frequency of words in a language to determine which words are more likely to be misspelled.

</br>Autocorrect is a helpful feature that can improve the accuracy and clarity of communication. It is a classic application of NLP and is used in many
software applications, including word processors, email clients, and web browsers.

### Code:
The code in this project implements an autocorrect function. The function takes a word as input and returns a list of possible corrections. The
function works by first creating a vocabulary of all the words in a text file. The vocabulary is then used to calculate the Jaccard similarity
between the input word and all the words in the vocabulary. The words with the highest Jaccard similarity are then returned as possible corrections.
</br>
The code is divided into the following parts:

**Importing libraries**: The first step is to import the necessary libraries. In this case, we need to import the following libraries:
- pandas
- numpy
- textdistance
- re
- collections
</br>

**Reading the text file**: The next step is to read the text file. The text file is opened in read mode and the lines are read one by one. Each
line is stripped of leading and trailing whitespaces and then the words in the line are extracted using a regular expression. The words are then
added to a list.


**Creating the vocabulary**: The next step is to create the vocabulary. The vocabulary is a set of all the words in the text file. The vocabulary
is created by using the set() function to convert the list of words to a set.


**Calculating the word frequencies**: The next step is to calculate the word frequencies. The word frequencies are calculated using the
Counter() function from the collections library. The Counter() function counts the number of times each word appears in the text file. 


**Calculating the Jaccard similarity**: The next step is to calculate the Jaccard similarity between the input word and all the words in the
vocabulary. The Jaccard similarity is a measure of the similarity between two sets. The Jaccard similarity between two sets is calculated by
dividing the number of elements that are in both sets by the total number of elements in the two sets.


**Returning the possible corrections**: The final step is to return the possible corrections. The possible corrections are the words in the
vocabulary that have the highest Jaccard similarity with the input word. The possible corrections are returned as a list. </br>

The autocorrect function can be used to correct misspellings in text. </br>

_Here are some additional details about the code_:</br>
- The textdistance library is used to calculate the Jaccard similarity between two sets. The Jaccard similarity is a measure of the similarity
between two sets. The Jaccard similarity between two sets is calculated by dividing the number of elements that are in both sets by the total number
of elements in the two sets.
- The collections library is used to calculate the word frequencies. The word frequencies are calculated using the Counter() function from the
collections library. The Counter() function counts the number of times each word appears in the text file.
- The autocorrect function is a simple function that can be easily modified to improve the accuracy of the corrections. The function is a valuable
tool for anyone who wants to improve the accuracy of their writing.

## Conclusion
Autocorrect is a powerful tool that can help users to communicate more effectively. It is a classic application of NLP and is used in many software
applications. Autocorrect is helpful because it can help users to avoid making mistakes and to communicate more effectively. It is a valuable tool
that can improve the quality of communication.</br>

Here are some additional benefits of autocorrect:
- It can help to improve the readability of text.
- It can help to reduce the number of errors in text.
- It can help to make text more consistent.
- It can help to make text more accessible to people with dyslexia or other learning disabilities.
</br>
Autocorrect is not without its drawbacks, however. One drawback is that it can sometimes make incorrect corrections. Another drawback is that it can
sometimes be slow or unresponsive. Despite these drawbacks, autocorrect is a valuable tool that can help users to communicate more effectively.
</br></br>

**Note**: I chose to implement this project as it is a powerful NLP application but also this covers a lot of statistical concepts covered in class.



# python-writing-for-loops
Create a loop to strip punctuation from the input file.

Position the insertion point in line 14 and press Enter.

Starting on line 15, type the code as shown.

This routine finds the first word in the input file, adds it to a list after stripping any punctuation, then does the same thing for every other word in the file. The loop ends when the last word in the file is read.

Line 15 initializes a counter you'll be incrementing in the loop to read through each index of the read_input list.
Line 17 is the start of the loop. Python will iterate through each word in the read_input list.
On line 18, all words are forced to lowercase so that they're uniform.
On line 20, the value at a certain index of read_input is set to whatever the word is, minus any extraneous punctuation. Basically, strip() removes the provided characters from the word, if they appear.
Line 21 increments the count by one, so that the list index for the next iteration of the loop also increments by one.
Write a loop to compare the input file to an existing English wordlist.

Position the insertion point in line 24 and press Enter.

Starting in line 25, enter the following code block:

This routine checks every word in the input text file for its presence in the wordlist. Once it finds a match, it checks to see if that word was already processed. If it was, the count goes up by one. If not, the word is added to the list with an initial count of one. When this routine is done, the word_count dictionary will be populated with key-value pairs, where each key is a unique word, and its associated value will contain the number of times the word appears.

On line 25, Python reads through each word it finds in the read_input list.
On line 26, each word is forced to lowercase.
On line 27, while still in the for loop, Python checks to see if the word in read_input also exists in read_wordlist.
If the word is in the wordlist, then line 28 checks to see if the word has not yet been added to the word_count dictionary.
If the word doesn't exist in word_count yet, line 29 sets the word's value to 1. (Remember, the word itself is used as the key.)
If the word has already been added to word_count, then line 31 increases the word count for that word by one.
Line 32 starts the else branch, which deals with words not in the word list. If a word is not in the word list, line 33 tells the for loop to continue on with the next iteration (the next word).
Write a loop to print the results to the console.

Position the insertion point in line 34 and press Enter.

Type the code as shown.

Lines 35 through 37 initialize objects used in the routine.
The choice string will be a yes or no input.
The items list will contain a sorted version of the dictionary you processed above. Each item in the list holds both the key and its value.
results_list will format the words and their counts in a more output-friendly context.
Line 40 checks every item in the list of sorted items. The slice tells the loop to only go through the first 50 values.
Line 41 evaluates whether the user says yes to suppressing common words from the results and the word at the first index (the dictionary key) is found in the COMMON_WORDS set. If both conditions are true, then the program will execute lines 42 through 44.
Line 42 assigns result to the word and concatenates it with some additional text, along with its count. The str() statement turns the integer count into a string for formatting purposes.
Line 43 appends this result to the results_list.
Line 44 prints the individual result to the console.
Lines 46 through 48 do essentially the same thing as 42 through 44, but every word is added.
So, the loop works through the first 50 items in the list. Once the list is sorted, these will be the 50 words with the highest frequency. If the user wants to suppress common words from the results, the results_list will not include the values in COMMON_WORDS. If the user doesn't want to suppress these words, they'll appear in the list. In both instances, the list is formatted so that every index holds a string with a word, its frequency, and "times" at the end. For example: the: 8 times is one possible result.

Stage some values so that you can test your for loops.

In lines 11 through 13, observe that read_input and read_wordlist are being set to contain arbitrary test strings.

These will eventually hold real values that you'll get from two text files, but for now you can test your loops with these staged lists. Remember that read_input will be the written work that your program analyzes, and read_wordlist will be the list of English words it gets compared to.

In the source code, scroll down to line 35 and change the value assigned to the choice variable to "n"

On the next line, change the items variable to sorted(word_count.items())

Python's built-in sorted() function creates a new list based on an existing structure, like a dictionary. Here, its first argument is the word_count variable you defined above. Because of .items() after the variable, each index of the list contains a tuple of two items: the dictionary's key (the word) and its value (the number of times the word appears). You'll later use sorted() to actually sort the results by descending frequency.

Test the program.

Run the program.

Verify that your program prints out the results_list: each word followed by the number of times it appears. Notice that, compared to the arbitrary values in read_input, these results have stripped punctuation and every character is in lowercase format.


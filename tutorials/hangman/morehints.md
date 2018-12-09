---
title: Hangman Hints Part 2
layout: jumbotron
back: walkthrough
next: #
---

# Some more hints

Use these hints only if you are *really* stuck.

- I suggest manually creating a list of words to choose from randomly. Also, it is easier to program if you don't use phrases.
- Use a ```for``` loop to cycle through each letter in the stored word in order to place letters in the correct position of the visible word. For example:
  - Scan through the word that the user is guessing. 
  - If the first letter in the stored word is equal to the guess, then set the first letter in the visible word to be the guess letter.
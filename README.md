Project for Networks & Distributed Systems, January 2023


To start this project I read the python documentation on how to make a socket

I first made a very simple client and server that could send messages to each other, then connected 
it to proj1.3700.network

It took me many tries to implement a solid guessing algorithm, but I set up my code so that I could
keep creating new functions and switching between them until I was able to get the flag with 
consistency

My final solution was to create 3 lists, one for each type of feedback(0, 1, or 2). 

The guessing function takes in the last guess, and its corresponding marks, and updates each list 
accordingly. 
    For each letter that got a 0, it's added to the words we know AREN'T in the list
    If it got a 1, it's added to words we know ARE in the list 
    If it got a 2, it's added to the variable answer

Then, the function iterates through every word in the list, and removes any word that couldn't work,
based on this information that it now knows (sort of like how a human would play Wordle)

My main challenge with this was that my function kept filtering out every word, without getting the
answer. It was also very hard to debug, because I obviously don't have time to look through every 
word in the list of 15,000. I had to rewrite my boolean statements (where the function was 
filtering) and make them easier to understand, and actually less efficient, in order to have it
actually guess the word consistently

I continuously tested my code in terminal by having my file print out helpful information, like
how many words were left in the list, what exactly the server and client said to each other, etc.





Homework 1

I knew that the program would need to be 3 parts:
1.) Check the rows
2.) Check the columns
3.) Check the 3x3 matrices

I called 3 seperate methods that check each of these parts and return a value of true or false. True meaning that everything checked out correctly, false meaning it didn't. If it was false in any of the 3 methods, it would add 1 to the counter "falseChecks".
 
Since any of the 3 parts being false makes the entire entered solution false, all we have to know is whether falseChecks ends up being 0 (making the soltion correct), or greater than 0 (making the solution false). 

To check the rows, I had one for loop to account for the current row, and another for loop to account for the current column. Then using a third for loop with variable k, I was able to test each value throughout a given row against all of the other values in that row. If there was a situation where the same number was repeated in the same row, it would add +1 to the variable check, which would then cause the method to return the boolean value of false. 

The check for the columns was almost identical to that of the rows, the only difference being that I had to switch the variables around so that the array would check itself vertically instead of horizontally. 

Lastly, the Matrix check. I tried a few different things before ultimately deciding that the easiest thing to do would be to convert each 3x3 array to a 1x9 and check them in a seperate method. I realize now that I may have been able to do the same with the first to parts and check them in the same method as the one for the matrix conversion, but I didn't see the need to spend all of that time re-doing the project.

The hardest part of the matrix check wasn't converting a 3x3 array, but rather moving across the 9x9 and picking out each 3x3 array. It ended up being a hard-to-read series of for loops, but it does the trick. 


-Chris Falco

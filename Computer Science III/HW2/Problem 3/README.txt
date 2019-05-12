Problem #3:
As I'm sure you would assume based on the point value of each question, problem 3 gave me the most trouble. Building the groundwork for how to begin the code was a problem in itself. I spent a lot of time just drafting out on paper different ways that I could logically check all possible combinations until finally coming to a decision. I used a set of facts that I came up with:

value:		Possible Moves:
j = 0		j + 1
j = 1 or 2	j + 1 or j - 1
j = 3		j - 1

i = 0		i + 1
i = 1 or 2	i - 1
i = 3		i + 1 or i - 1

using these facts, I created 9 possible rules:

					Rules
	
Key:		Value:					Possible Moves:	
a = i + 1	i = 0 & j = 0				a, c				
b = i - 1	i = 0 & (j = 1 or j = 2)		a, c, d
c = j + 1	i = 0 & j = 3				a, d
d = j - 1	(i = 1 or i = 2) & j = 0		a, b, c
		(i = 1 or i = 2) & (j = 1 or j = 2)	a, b, c, d
		(i = 1 or i = 2) & j = 3		a, b, d
		i = 3 & j = 0				b, c
		i = 3 & (j = 1 or j = 2)		b, d, d
		i = 3 & j = 3				b, d

With these rules, I began to construct my code. I created a for loop that would run through a 4x4 array containing the chart you gave us. Inside of the inner loop, I put all of the rules that I listed. if the current value of i an j met a certain rule, it would run that if statement's code. Depending on which rule it met, there could be anywhere from 2 to 4 doors to go through next. The idea is, the code goes through all possible doors over the course of four very similar methods (one for each digit in the 4 digit combo), and brings back the max value for each combination. Each method then tests the max values against each other to see which one is the true max to return to the previous method, and then eventually outputs the correct highest combination. It's very complex. In some ways, I think it could've been easier. I keep wondering if there was a way to loop the process so that I wouldn't have had to make 4 methods of practically the same code. They had slight differences, though. For example, one problem I ran into was figuring out how to stop the combination from going back to a spot it had already been. I did this by using the variables iStep1, iStep2, jStep1, jStep2. I used them to check if the position on step 3 was the same as the position on step 1, and if the position on step 4 was the same as step 2. If they were, the code would return a value that would never pass the tests to be considered as a possible combination. 

I thought that once I got done with the correct highest combo output, I would basically just be able to flip a few things around and add some extra if statements to get the lowest combo. The problem with that was I realized that I couldn't return two values from a method (as far as I know). This was the moment that I understood at the very least, I would have to double my code from 500 lines to 1000 with extra methods for the lowest combo steps. It may not have been the most effecient way of getting it done, but it worked. I just created the additional methods, flipped the signs around in the comparing statements, a few other minor tweaks, and I got the desired output for the lowest combo as well.

Despite the fact that it is almost 1000 lines of code, it does return the correct answer so I'm proud of it. It was a difficult challenge to overcome, so to see it work the way that I planned was nice. In the future I may try to work on optimizing it to make it smaller, more readable code.

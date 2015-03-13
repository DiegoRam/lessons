PseudoCode
__________

PeusoCode is basically a technique which allows us to represent algorithms in terms of a more natural language instead using an specific programming one, like python or c++.

That’s why we can say that PseudoCode is extremely similar to the English or any other language you like to talk into.

Since we already know the fact that all computers are dumb, but are really good to repeat things, we create this kind of convention to express our ideas neat and clearly. Doing so, we will be able to share our ideas and understand other people’s.

## Our Mantra
		divide and conquer

It’s pretty known that splitting a problem out into several smaller pieces would be better to solve the problem like a whole.
		“if you have to get clean you room, it’s better to start with your toys, AND THEN with your clothes, AND THEN with your shoes, AND THEN with books, AND SO ON.”
Always about a problem like little pieces, attack them one by one, and conquer it!

Said so, let’s say there are six basic structure which allow us represent the steps on a computer:

## IF THEN ELSE

This is a decision structure: here we need to perform an action due to a condition:

		“If it’s raining, then I need to get my umbrella. If it doesn’t I need to get my hat”.

Let’s see how our convention is going to write down this kind of things.

	
		- IF(raining == True) THEN
		|  get my umbrella
		|
		- ELSE
		|  get my hat
		|
		- ENDIF

There are so many way to use it according to your particular problem.

		- IF(raining == True) THEN
		| get my umbrella
		- ENDIF
		- takethebus()

Prior example says to us that we’ll always takeabus() but, if we check the wheather and notice that it’s raining, we should get our umbrella.

## Initialize variables

Let’s keep in mind we always have to initialize (using SET clause) the variable we are going to use into our programs.

		SET raining to False
		SET candies_in_my_pockets_count to 3
		- IF(raining == True and candies_in_my_pockets_count == 3) THEN
		| get more candies
		- ELSE
		| eat a candy
		- ENDIF

## FOR

This loop is a specialized construct for iterating a specific number of times, often called a “counting” loop.  Two keywords, FOR and ENDFOR are used. The general form is:

		- FOR iteration bounds
		| sequence
		- ENDFOR

Examples

		FOR each month of the year (good) 
		FOR month = 1 to 12 (ok)
		FOR each employee in the list (good) 
		FOR empno = 1 to listsize (ok)


Even better we can embed the structures each other

		SET total to zero 
		- FOR number = 1 to 10
		| - IF(number % 2 == 0)
		| |  total = total + number
		| - ENDIF
		- ENDFOR
		PRINT total

## WHILE

The WHILE construct is used to specify a loop with a test at the top. The beginning and ending of the loop are indicated by two keywords WHILE and ENDWHILE. The general form is:

		- WHILE Population < Limit
		| Compute Population as Population + Births - Deaths
		- ENDWHILE

Example

		- WHILE employee.type NOT EQUAL manager AND personCount < numEmployees
		| INCREMENT personCount
		| CALL employeeList.getPerson with personCount RETURNING employee
		- ENDWHILE

## CASE 

A CASE construct indicates a multiway branch based on conditions that are mutually exclusive. Four keywords, CASE, OF, OTHERS, and ENDCASE, and conditions are used to indicate the various alternatives. The general form is:

		- CASE expression OF
		| condition 1 : sequence 1 
		| condition 2 : sequence 2 
		| … 
		| condition n : sequence n 
		- OTHERS: 
		| default sequence
		- ENDCASE

Example

		- CASE month OF
		| 1: friendly_month = “January”
		| 2: friendly_month = “Febrary”
		| 2: friendly_month = “March”
		| …
		- OTHER
		| friendly_month = “Invalid month number”
		- ENDCASE

## REPEAT-UNTIL

This loop is similar to the WHILE loop except that the test is performed at the bottom of the loop instead of at the top. Two keywords, REPEAT and UNTIL are used. The general form is:

		- REPEAT
		| sequence
		- UNTIL condition

The “sequence” in this type of loop is always performed at least once, because the test is performed after the sequence is executed. At the conclusion of each iteration, the condition is evaluated, and the loop repeats if the condition is false. The loop terminates when the condition becomes true. 

Example

		SET my_belly_hurts to False
		- REPEAT
		| eat a cookie
		- UNTIL my_belly_hurts == True


### Exercises


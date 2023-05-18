## Basic Counting Techniques
1. In a class of 20, the number of ways of selecting a president, vice-president, secretary and treasurer is…
   $10(19)(18)(17) = 116,860$ ways
   
2. A burger machine offers a serving Of soup, sandwich and beverage. There are two kind of soups (corn or asparagus), 4 sandwiches (chicken, ham, mushroom, and tuna) and 5 beverages (coffee, tea, milk, coke and orange) to choose from. Then the number of possible…
   $2(4)(5) = 40$ ways
   
## Principles of Counting
$n_1 n_2$ ways

### Examples:
1. If in climbing a certain mountain, there are 5 trails that could be followed in going to the top and 4 trails in going down, in how many ways can the tip be done?
   $n_1 = 5$
   $n_2 = 4$
   $n_1 n_2 = 5(4) = 20$ ways
   
2. Certain government employees are classified into two categories according to sex and four categories according to marital status. List the different ways of classifying one Of the employees.
   $n_1 = 2$
   $n_2 = 4$
   $n_1 n_2 = 8$ ways

## Generalization of Principle of Counting
$k$ steps made into $n_1$ ways … $k^{th}$ step made into $n_k$ ways
$n_1 n_2 … n_k$ ways

### Example
1. How many dinners consisting of a soup, viand, dessert and a drink are possible if we can select from 4 soups, 10 viands, 5 desserts and 4 kinds of drinks?
   $n_1 = 4$
   $n_2 = 10$
   $n_3 = 5$
   $n_4 = 4$
   $n_1 n_2 n_3 n_4 = 4(10)(5)(4) = 800$ ways
   
2. A test is composed of 10 multiple-choice question, with each having four possible answers. In how many ways can a student answer all the questions?
   $n_1$ to $n_{10} = 4$
   $n^{10} = 4^{10} = 1,048,576$ ways
   
3. A college freshman must take a Mathematics, English and Social Science course. If he may select any of 3 Mathematics courses and of 4 English courses and any of 5 Social Sciences courses, in how many ways can he arrange his program?
   $n_1 = 3$
   $n_2 = 4$
   $n_3 = 5$
   $n_1 n_2 n_3 = 3(4)(5) = 60$ ways
   
4. How many 3-digit numbers can be formed from the four digits 0,1,2,3 if …
	1. …no two digits are to be the same?
	   $n_1 = 3$
	   $n_2 = 3$
	   $n_3 = 2$
	   $n_1 n_2 n_3 = 3(3)(2)$ ways
	   
	2. …the numbers are odd?
	   $n_1 = 2$
	   $n_2 = 2$
	   $n_3 = 2$
	   $n_1 n_2 n_3 = 8$ ways
	   
	3. …the numbers are even?
	   $18 - 8 = 10$ ways
	   
	4. …repetition of digits are allowed?
	   $n_1 = 3$
	   $n_2 = 4$
	   $n_3 = 4$
	   $n_1 n_2 n_3 = 3(4)(4) = 48$ ways

## Permutation
Arrange of a group of things in definite order

$n$ distinct objects arranged in:
$n! = n(n - 1)(n - 2)(n - 3)(n - 4) … (3)(2)(1)$

### Example
1. The letters a, b, and c have the following possible arrangements or permutations:
   $abc, acb, bac, bca, cab, cba$
   
2. The number of ways of arranging the digits 1, 2 and 3 where two are taken at a time is 6. The 6 arrangements are…
   $12, 13, 21, 23, 31, 32$
   
3. In how many ways can four books (Math, English, History and Science) be arranged on a shelf?
   $4! = 24$ ways
   
4. In how many ways can 3 students be seated in a row?
   $3! = 6$ ways

## Arrangement of $n$ Objects Taken at $r$ Time
Consider the number of permutations that are possible by considering $r$ letters at a time

$n$ distinct objects arranged in:
$n(n - 1)(n - 2) … (n - r + 1)$ ways

$n$ objects taken at $r$ time:
$nP_r = \frac{n!}{(n-r)!}$

### Example
1. In how many ways can 5 starting positions on a PBA team be filled with 12 men who can play any of the positions?
2. 2. How many permutations can be made from the letters in the word "SUNDAY" if…
	1. …4 letters are used at a time
	   $6P_4 = \frac{6!}{6-4}! = 360$ ways
	   
	2. …all letters are used
	   $6P_6 = \frac{6!}{6-6}! = 6! = 720$ ways
	   
	3. …all letters are used but the first is a vowel
	   $2P_1 * 5P_5 = 240$ ways
	   
3. 

## Summary
**Permutation**
$nP_n = P(n,n) = n! = n(n - 1)(n - 2) … (2)(1)$

**Arrangement of $n$ Objects Taken at $r$ Time**
$nP_r = \frac{n!}{(n-r)!}$


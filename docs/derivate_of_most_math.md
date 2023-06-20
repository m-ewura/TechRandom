## Prompt Engineering Has Come A Long Way ... Hasn't It?

In the begining there was `counting numbers` and there was space.
1. Can we have a placeholder to replace space?<br>
  Then there was `whole or natural numbers`

2. If we should go one way, can we go the opposite way?<br>
  Then there was `integers`

3. Can we share your apple? (Adam to Eve 😀)<br>
  Then there was `rational numbers`

4. What do you think the diagonal of a square will be?<br>
  Well, that's irrational! `irrational numbers`

5. What will happen when we square root a negative number?<br>
  Hm, That is not a real number!<br>
  Can it exist as an imaginary number? 🤔<br>
   $`i = \sqrt-1`$ &nbsp; `imaginary numbers`<br>
   $`i^2 = -1`$

6. Can we add an `imaginary number` to a `real number`?<br>
  Woh! Take your time.<br>

&#9432; &nbsp; It's impossible till it's possible.<br>
Then there was `complex numbers`

<img width="450" alt="Complex Numbers" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-complex-nos-6.jpg">

There are many other methods derived from $`QnA`$s and fine-tuning.<br>
- &nbsp; &nbsp;-----> &nbsp;Can it go the other way?
- &nbsp; &nbsp;-----> &nbsp;Can I use it with something I know?
   
Say, we wanted to know the average volume of sound in a room filled with people<br>
talking at different volumes.<br>

$$\mu = {\sum x \over n}$$

where: $`\mu`$ = Average, $`\sum`$= Sum of volumes, $`n`$ = Count($`n\underline{o}`$) of volumes<br>

<img width="450" alt="Average of n values" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-average-7.jpg">

7.1. &nbsp;How far on average, are all values from the middle?

<img width="450" alt="Mean Deviation" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-mean-7-1.jpg">

7.2. &nbsp;How about the reciprocal of the volumes... Can we have an average for that?<br>
Sure. We can even have the reciprocal of the average 😀. `Harmonic Mean`<br>
  This method is good for handling big outliers.

7.3. &nbsp;How about when we want to compare different properties? `Geometric Mean`<br>

<img width="450" alt="Geometric Mean" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-geometric-mean-7-3.jpg">

`Geometric Mean` can also be used to calculate mean of different large values.<br>
In example 2,<br>
&nbsp; &nbsp;we confirm the saying 'A child is half way between a Cell and the Earth'.

7.4. &nbsp;We can also find the rate of change or slope between two points, $`\Delta y \over \Delta x`$<br>
as well as form a triangle from the change...given the $`x`$ and $`y`$ values,<br>
and calculate the hypotenuse, using pythagoras theorem. We can then perform<br>
trigonometry operations on it. Like, finding the angle $`\theta`$ . You get the idea.

<img width="450" alt="Slope" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-slope-7-4.jpg">

8.1. &nbsp;What is the probability that search engines can read your mind? Think about it.<br>

-----> _event can be one or more outcomes_<br>

$$Probability\space of\space an\space Event 
= {n\underline{o}\space of\space ways\space it\space can\space happen\space \over total\space n\underline{o}\space of\space outcomes}$$ 

<img width="450" alt="Probability Line" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-probability-line-8-1.jpg">

-----> _the sum of probability of all possible outcomes = 1_ <br>

$$P(A) + P(\hat A) = 1$$

where: $`P(A)`$ = event(s), $`P(\hat A)`$ = complement of event(s) or unwanted possible outcome(s)<br>

- &nbsp; &nbsp;-----> &nbsp;What is the probability of creating random words?<br>
(Words that can at least be pronounced. Let's start with (4) letter words.)<br>
- &nbsp; &nbsp;-----> &nbsp;How about we say, the word should have at least one vowel? 🤔<br>
- &nbsp; &nbsp;-----> &nbsp;Or what's the frequency of letters that follow another letter?<br>

$$Relative\space Frequency = {how\space often\space something\space happens \over total\space outcomes}$$

-----> _when there are&nbsp; $`M`$ ways to do something and&nbsp; $`N`$ ways to do another,<br>
then there are&nbsp; $`M * N`$ ways to do both_

8.2. &nbsp;Probability of (2) Events A and B, where both are independent, is

&nbsp; $`P(A\space and\space B) = P(A) * P(B)`$

8.3. &nbsp;Probability of (2) Events, where Event B is dependant on Event A,<br>
will be (Pr of eventA) * (Pr of eventB given eventA)

&nbsp; $`P(B\space and\space A) = P(A) * P(B \mid A)`$

From this, we can derive,<br>

&nbsp; $`P(B \mid A) = {P(B\space and\space A) \over P(A)}`$

and&nbsp; $`P(A) = {P(B\space and\space A) \over P(B \mid A)}`$

8.4. &nbsp;Probability of A or B, gives us

&nbsp; $`P(A\space or\space B) = P(A) + P(B)`$

or when there's a mutually inclusive possibility,

&nbsp; $`P(A) + P(B) - P(A \cap B)`$

8.5. &nbsp;Can we find probability when we know certain other probabilities?

&nbsp; $`P(A \mid B) = {P(A) * P(B \mid A) \over P(B)}`$

8.6. &nbsp;How about the probability of any combination?

-----> _combination of (2) or more things, regardless of the order of combination = Combination_

-----> _combination of (2) or more things, with regard to order of combination = Permutation_

- Combination of a pin to unlock your phone is ___permutation___ .
- Combination of white and yellow socks is ___combination___ . White and yellow socks?<br>

<br>Can you think of a better example? Something along those lines.<br><br>

-----> _**combination** and **permutation** can both have repeating values or not ._
- Terms
  - $`!`$ &nbsp; is factorial of the number
  - n &nbsp; is no. of things to choose from
  - r &nbsp; we choose **r** of them<br>
  
**Permutation Formulae**:<br>
with repetition:

$$n^r$$

without repetition:

$$P(n,r) = ^{n}P_{r} = nPr = {n! \over (n-r)!}$$

**Combination Formulae**:<br>
with repetition:

$$(r + n - 1)! \over r!(n-1)!$$

without repetition:

$$C(n,r) = ^{n}C_{r} = nCr = \binom{n}r = {n! \over r!(n-r)!}$$

<img width="450" alt="Permutation and Combination" src="https://github.com/ewurabapotez/TechRandom/blob/main/assets/images/d-combo-8-6.jpg">

Do you remember $`{change\space in\space Y \over change\space in\space X} = {dy \over dx}`$ formula?

9. TLDR:<br>
- Exploration of questions and answers (QnA), refining and fine-tuning.





























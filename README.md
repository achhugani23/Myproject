STAT 428: Homework 1: <br> Testing Rmd and homework submission
================
Chhugani, Akhil, chhugan2 <br> Collaborated with: Rohan Kapatkar, kapatka2
Due Week 3, Wednesday January 31 by 5:59 PM on Compass

-   [Exercise 1:](#exercise-1)
-   [Exercise 2:](#exercise-2)
-   [Exercise 3:](#exercise-3)
-   [Exercise 4:](#exercise-4)
-   [Exercise 5](#exercise-5)

------------------------------------------------------------------------

Your first homework is to get up to speed with writing documents in RMarkdown and to familiarize yourselves the HW submission format and process.

Exercise 1:
-----------

For this homework, it will be easiest for you to save [this `.Rmd` file as a template](428HW1.Rmd) and make necessary additions and/or deletions. *(Make sure you use the naming conventions for file names and contents)*

Your tasks!

-   Save [this `.Rmd` file](428HW1.Rmd) using the naming conventions for homework assignments.
-   Open the file in RStudio
-   Change the name of the author above to yours
-   Add any collaborators anytime you have worked with someone on this assignment
-   Click Knit HTML
-   After doing all the above steps, add an appropriate section marked `Solution` for Exercise 1, remove any unnecessary text that should not be included in the report and a sentence to your solution section so that your report states that you have followed the tasks listed in Exercise 1.

-   Continue doing the remaining exercises, editing the document in RStudio to write out your solutions, appropriately marked as Solutions.
-   Finally, review the [formating and submission instructions](https://compass2g.illinois.edu/bbcswebdav/pid-3028361-dt-content-rid-31752712_1/courses/stat_428_120181_161673/1_Info/Syllabus/homework_policy.html) and **Submit your homework**.

Exercise 2:
-----------

This exercise has several parts about RMarkdown syntax. You may look into the [Scribing Reference](https://compass2g.illinois.edu/bbcswebdav/pid-3028398-dt-content-rid-31752865_1/courses/stat_428_120181_161673/1_Info/Syllabus/Tutorial/2A_RMarkdown_Tutorial.html) as you work through this exercise. 1. Write two sentences below about yourself?

**Solution: **My name is Akhil Chhugani I am currently studying Computer Science. I am from New Jersey and came here because of the great engineering school.

1.  Copy and paste the above two sentences. Make one sentence **bold** and the other *italic*. Separate the two sentences by a blank line.

**Solution: ** **My name is Akhil Chhugani I am currently studying Computer Science.**

*I am from New Jersey and came here because of the great engineering school.*

1.  What's your favorite website?
    1.  Create a hyperlink anchored to text 'My favorite website' to your favorite website.

    **Solution: ** [My favorite website](https://www.netflix.com/)
    1.  Create a hyperlink anchored by the URL to your favorite website.

    **Solution: ** <https://www.netflix.com/>
2.  What character is used to denote headers?

**Solution: ** \#

1.  Write a quoted statistics or probability joke. *(Remember, to acknowlege the reference to where you found the joke)*. *If you are having a hard time finding one, just quote the paragraphs below:*

**Solution: **

> -   Girlfriend: Our love is like a Poisson distribution, rare and special. Out of all the men in the world, we found each other.
> -   Boyfriend: Hmm, I think I'd describe it more like a geometric distribution. I failed with all the other women in our class but I knew there would eventually be a success...you!

1.  Write Computer Type for running 2+3 in R

**Solution: ** `2 + 3`

1.  Write a bulleted list of top 3 reasons you chose this course
    **Solution: **

    -   Stats Minor
    -   Wanted to learn some R
    -   Was interested in statistical computing because of my CS background

2.  Write an itemized list of your top three fears in this course. You may use sub-list if necessary!
    **Solution: **
    1.  Not understanding R fast enough
    2.  Too much work
    3.  Not enough stats knowledge coming in
3.  Find an image on web or create one using R, of the hypergeometric distribution. Insert the image here.
    **Solution: ** ![](distribution.png)
4.  Can you find a way to resize the image in RMarkdown?
    **Solution: **

``` r
knitr::include_graphics("distribution.png")
```

<img src="distribution.png" width="400px" />

1.  Write three separate code chunks named A, B, C where

-   code chunk A shows only results but no code
-   code chunk B shows only the code but does not run it
-   code chunk C neither shows the code nor the results but does run the code echo=FALSE, eval = FALSE, include=FALSE

**Solution Chunk A: **

    ## [1] 10

**Solution Chunk B: **

``` r
  x = 2 + 3
  y = x * 2
  print(y)
```

**No Solution shown in Chunk C**

*(You may include simple code for adding 2 and 3 or more elaborate code like we did in class.)*
12. Using Latex, write the equation for the likelihood function *L*(*θ*) that corresponds to *n* i.i.d Bernoulli random variables *X*<sub>*i*</sub>.
$$
\\begin{eqnarray}
L(\\theta) = \\prod\_{i=1}^n \\theta^{x\_i}(1-\\theta)^{1-x\_i}  
\\end{eqnarray}
$$
 13. Describe in one sentence your experience doing this exercise.

This exercise was good for getting an understanding of RMarkdown.

Exercise 3:
-----------

Mark whether the following statements pertaining to this class are True or False. If False, make sure you know what the true statement is. You may need to refer to the Syllabus to answer the following questions.

1.  **True/False**: Piazza should be used as much as possible for questions pertaining to course administration and general course information.
    **Solution: **True
2.  **True/False**: Email is the fastest way to get questions related to homework as well as general questions answered.
    **Solution: **False
3.  **True/False**: The exam dates and location are
    -   Exam 1: Week 7, Monday, Oct 9, in class
    -   Exam 2: Week 14, Friday, Dec 01, in class
        **Solution: **False
4.  **True/False**: Homework and exams can be eaisly made up after the deadline by sending an email to the instructor or the TA requesting this. Such emails will be answered instantly.
    **Solution: **False

Exercise 4:
-----------

**Simple R questions: ** Some of the questions below can be answered with very little or no programming. However, write code that outputs the final answer and does not require any additional paper calculations. For example, suppose I ask for how many numbers are in the vector, `x=c(1,9,2,8,10,12)`. Do not count the numbers in the vector, instead have R count by coding `length(x)`. *('c()' is a function to create vector in R; 'length()' is a function to calculate the length of a vector (refer [here](http://www.statmethods.net/input/datatypes.html) or google).)*

R has a built-in character vector of US State divisions, `state.division`. Use this character vector and R's character functions (refer [here](http://www.statmethods.net/management/functions.html) or google) to answer the following questions.

1.  What is the longest state division name (including spaces) and how long is it?
    **Solution: **

``` r
divs = levels(state.division)
lens = nchar(divs)
m = which.max(lens)
print(lens[4])
```

    ## [1] 18

``` r
print(divs[4])
```

    ## [1] "East South Central"

1.  List all the state division names that are more then one word. How many are there?
    **Solution: **

``` r
outputs = character()
for (i in 1:length(divs)){
  l = strsplit(divs[i], " ")
  if (sapply(l, length) > 1){
    outputs <- c(outputs, divs[i])
  }
}
print(outputs)
```

    ## [1] "New England"        "Middle Atlantic"    "South Atlantic"    
    ## [4] "East South Central" "West South Central" "East North Central"
    ## [7] "West North Central"

``` r
print(length(outputs))
```

    ## [1] 7

1.  How many states are there in the "Mountain" division? How many in the Atlantic division (combining Middle and South)?
    **Solution: **

``` r
mountain = sum(state.division == "Mountain")
midAtlantic = sum(state.division == "Middle Atlantic")
southAtlantic = sum(state.division == "South Atlantic")
print(mountain + midAtlantic + southAtlantic)
```

    ## [1] 19

1.  List all the US State division names, where all of the upper and lower case `a's` are replaced with a capital `Z`.
    **Solution: **

``` r
print(gsub("a","Z", divs))
```

    ## [1] "New EnglZnd"        "Middle AtlZntic"    "South AtlZntic"    
    ## [4] "EZst South CentrZl" "West South CentrZl" "EZst North CentrZl"
    ## [7] "West North CentrZl" "MountZin"           "PZcific"

Exercise 5
----------

Continuing with the previous exercise, R also has a built-in matrix of different types of data of every US states, `state.x77`. Use this matrix and R's built in functions and **vector calculation** to perform the following tasks.

1.  Output only the second column of the matrix and store it in the numeric vector `capita`. This vector indicates the per capita income (1974) of every US states.
    **Solution: **

``` r
capita = as.numeric(state.x77[,2])
print(capita)
```

    ##  [1] 3624 6315 4530 3378 5114 4884 5348 4809 4815 4091 4963 4119 5107 4458 4628
    ## [16] 4669 3712 3545 3694 5299 4755 4751 4675 3098 4254 4347 4508 5149 4281 5237
    ## [31] 3601 4903 3875 5087 4561 3983 4660 4449 4558 3635 4167 3821 4188 4022 3907
    ## [46] 4701 4864 3617 4468 4566

1.  What is the average per-capita income of US (1974)?
    **Solution: **

``` r
print(mean(capita))
```

    ## [1] 4436

1.  What is the average per-capita income of the "New England" division of states?
    **Solution: **

``` r
inds = which(state.division == "New England")
states = state.name[inds]
ne_capitas = state.x77[inds,2]
print(mean(ne_capitas))
```

    ## [1] 4424

1.  Which state has the highest per-capita income? Which division does this state belong to?
    **Solution: **

``` r
max_ind = which(capita==max(capita))
print(state.name[max_ind])
```

    ## [1] "Alaska"

``` r
print(state.division[max_ind])
```

    ## [1] Pacific
    ## 9 Levels: New England Middle Atlantic South Atlantic ... Pacific

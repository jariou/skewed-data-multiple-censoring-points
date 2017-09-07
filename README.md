
#Models for Left Skewed/Right Skewed data with Multiple Censoring Points


Most actuaries predominantly study right skewed 
losses due to the nature of insurance policies. 
However, some actuaries working for the government 
agencies may occasionally see unconventional loss 
data. For example, benefit grants given to low 
income population (e.g. veterans) are limited to 
a certain amount of spending. These grants are 
considered financial expenditures (or losses) to 
the government agencies. While this financial-benefit 
model has some similarities with the insurance model, 
there are some known differences. A data set on 
veterans benefit is provided by ND Department of 
Veterans Affairs for the period 2006-2009 (see 
Figure below).  The benefit limit of $1000 was 
introduced in year 2008. Prior to 2008, there was 
a benefit limit of $750.  
  

Year 2006-2009; 225 observations; 38% censoring; 
2 censoring levels: $750 and $1000.


Research question: The ND State Agency wants to know 
what is the sensitivity of the average amount of benefit 
to the number of censored data? When is the right time 
to introduce a new benefit limit? What should be the 
proposed value of a new limit (a new censoring point)?   

Can we develop a probability distribution for this type 
of benefit data and answer the above questions using an 
extensive simulation study?  

The extension of this problem can be looked at in the 
insurance loss modeling where there are different 
policy limits and the right tail of the loss 
distribution has multiple right censoring points (but 
not all observations are censored at the censoring 
points). For example, ISO Loss Data (see below) have 
8 censoring points. Censored amount is listed in $’1000s 
of dollars. Number of censoring data points are listed 
in parentheses. 
      

I have worked with this data before and developed the 
following pdf with my other two collaborators.   

- Let ${\bf x}=(x_1, x_2, \ldots, x_n)$ denote a vector of 
$n$ independent observations

- Let the vector ${\bf c}=(c_1, c_2, \ldots, c_M)$ 
represent the $M$ different right censoring points and 
let ${\bf \alpha}= (\alpha_1, \alpha_2, \ldots, \alpha_M)'$
be the corresponding vector of censoring probabilities.

- The conditional probabilities aere computed as 
$\alpha_i = P(X=c_i|X>c_i)$, for $i = 1, 2, \ldots, M$

- Then, the random variable $X$ has the following PDF

$$
f_X(x,{\bf c}|{\bf \theta}, {\bf \alpha})=
\begin{cases}
f_X(x,\{\bf c}|{\bf \theta}, {\bf \alpha})=,\\
x(n-1)\\
x(n-1)
\end{cases}
$$

I am not sure if this approach is correct. Although 
the f() integrates to 1, so it is a legitimate 
probability distribution function. We tried to model 
this using mixture models and were not so successful 
with our simulation study. 

Maybe you have some other ideas on how to tackle 
this type of loss data.  

Download Link: https://assignmentchef.com/product/solved-aglm-assignment-n-o-3
<br>
Applied Generalized Linear models

Task 1                                                                                                                                                6 points

The data in the file frequency.cvs was collected in January-November 2018 with an online survey open to anyone. Respondents were motivated to take the survey by the opportunity to receive personalized results.

The data set contains the following variables:

<ul>

 <li>Q2: “I think about how my actions affect the environment”</li>

</ul>

(5 point rating scale: 1=never, 2=rarely, 3=occasionally, 4=often, 5=always)

<ul>

 <li>education “How much education have you completed?”</li>

</ul>

(1=Less than high school, 2=High school, 3=University degree, 4=Graduate degree)

<ul>

 <li>urban: “What type of area did you live when you were a child?”</li>

</ul>

(1=Rural (country side), 2=Suburban, 3=Urban (town, city))

<ul>

 <li>gender: “What is your gender?”</li>

</ul>

(1=Male, 2=Female, 3=Other)

<ul>

 <li>age: “How many years old are you?”</li>

 <li>race: “What is your race?”</li>

</ul>

(11=Asian, 12=Arab, 13=Black, 14=Indigenous Australian, 15=Native American, 16=White, 17=Other)

<ul>

 <li>married: “What is your marital status?”</li>

</ul>

(1=Never married, 2=Currently married, 3=Previously married)

<ul>

 <li>familysize: “Including you, how many children did your mother have?”</li>

</ul>

For all the variables, the value 0 is used to represent missing values.

We would like to test whether there is an association between <em>Q</em>2 and the other variables in the data set using the ordered logistic regression model.

<ul>

 <li>Import the data. Recode the variable race so that all the categories that have a frequency lower than 100 are combined into the category “other”. Recode missing values in the dataset into NA.</li>

 <li>Consider the OLRM intercept model having <em>Q</em>2 as the dependent variable (i.e., the OLRM without explanatory variables). Write down the formula of the model and compute the estimate of the intercept parameters without estimating the model.</li>

 <li>Use the backward selection procedure to select the best fitting OLRM. The code we used in the practical session on OLRM returns an error. Explain why the error occurs and correct the code so that you can select the best fitting model.</li>

 <li>Consider the best fitting OLRM returned by the backward procedure. Test its goodness of fit using an adequate test.</li>

 <li>Interpret the model coefficients.</li>

</ul>

<h2>Task 2                                                                                                                                                4 points</h2>

The assumption of parallel slopes (or proportional odds) underlying the OLRM implies that the coefficients describing the relationship between the ordinal dependent variable and the explanatory variables are the same between any pair of adjacent categories.

Develop a procedure to informal assess the assumption of parallel slopes.

<ul>

 <li>Describe the procedure and its logic.</li>

 <li>Apply the developed procedure to check whether the parallel slopes assumption is matched by the data in Task 1 and the explanatory variables included in the best fitting model (Task 1, point 2).</li>

</ul>

(Hint: Think about the assumption in terms of logit or odds ratio. Base the procedure on the estimation of binary logistic regression models (one for each category but <em>M</em>) having the form

The dependent variable <em>Y<sup>m </sup></em>is a binary variable taking value 1 if the ordinal dependent variable <em>Y </em>is greater than <em>m</em>, and 0 otherwise. Consider one explanatory variable at a time.)

<h2>Task 3                                                                                                                                                7 points</h2>

The data set medpar.csv is an excerpt from US national Medicare inpatient hospital database. It contains 1495 observations on the following variables:

<ul>

 <li>los: length of hospital stay (in days)</li>

 <li>hmo: patient belongs to a Health Maintenance Organization (1), or private pay (0)</li>

 <li>white: patient identifies themselves as primarily Caucasian (1) in comparison to non-white (0)</li>

 <li>age80: patient age 80 and over (1), or age <em>&lt; </em>80 (0)</li>

 <li>type: a three-level explanatory variable related to the type of admission</li>

</ul>

(1 = elective, 2 = urgent, and 3 = emergency)

We would like to investigate whether there is an association between the length of hospital stay and the other variables.

<ul>

 <li>Import the data. Based on the descriptive statistics, do you expect that there is a significant relation between los and type? Justify your answer.</li>

 <li>Estimate a Poisson regression model with los as dependent variable and type as explanatory variable. Name this model Model 1. Interpret the parameters of the model (including the intercept).</li>

 <li>Add to the model in (2) the explanatory variables age80, hmo and white. Name the resulting model Model 2. Test whether Model 2 has a better fit than Model 1.</li>

 <li>Interpret the parameter related to the variable age80.</li>

 <li>Test whether the equi-dispersion assumption is matched by the data. If that is not the case:</li>

</ul>

<ol start="3">

 <li>Estimate an adequate model including all the explanatory variables. Name this model Model 3. ii. Compare the results of Model 2 and Model 3. Are they the same?</li>

</ol>

<h2>Task 4                                                                                                                                                3 points</h2>

Could you think of a test for equi-dispersed data based on the comparison of two models rather than testing the over-dispersion parameter <em>α </em>of the negative binomial regression model?

<ul>

 <li>Define the null and the alternative hypotheses, the test statistic and the rejection region. Explain the logic of the test.</li>

 <li>Apply the test to the data in Task 3.</li>

</ul>
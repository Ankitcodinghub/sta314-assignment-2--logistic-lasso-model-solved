# sta314-assignment-2--logistic-lasso-model-solved
**TO GET THIS SOLUTION VISIT:** [STA314 Assignment 2- Logistic Lasso Model Solved](https://www.ankitcodinghub.com/product/sta314-assignment-2-logistic-lasso-model-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;96408&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;STA314 Assignment 2- Logistic Lasso Model  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
<ol start="0">
<li>The task
Your task for this assignment is to program up functions to compute the logistic Lasso using coordinate descent on the the penalized iteratively reweighted least squares algorithm. Please note: You will need to modify the derivation of coordiante descent to allow for weights!

You will then build the helper functions required to add your algorihm as a parsnip model so that it can be used in a tidymodels workflow.

You are to then to write a short vignette that explains how to use your function within a tidymodels workflow to perform classification. This should include how to tune the model.

This vignette should not call any of the functions in the file functions.R directly, but should instead have the following code (or its equivalent) somewhere near the beginning

From that point forward, the vignette should use the functions you have written only through the tidymodels interface you have built.

The functions

You only need to write two main function (although you’re welcome to use helper functions as long as they are documented appropriately). It should have the following signature:

ret &lt;- fit_logistic_lasso(x, y, lambda, beta0 = NULL, eps = 0.0001, iter_max = 100) where: • x: matrix of predictors (not including the intercept)
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
source(“functions.R”) source(“make_tidy.R”)

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
• y: vector of data

• lambda: penalty

• beta0: initial guess

• eps: parameter for stopping critereon

• iter_max: maximium number of iterations

• ret A list containing the members intercept, beta, and lambda

<pre>ret &lt;- predict_logistic_lasso(object, new_x)
</pre>
where:

• object: Output from fit_logistic_lasso

• new_x: Data to predict at (may be more than one point!) • ret A list containing the intercept and beta

Unit tests

The exact unit tests that will be used for marking will not be released.

The purpose of these tests is to ensure that the functions work as indicated. Below is some skeleton code for

a unit test for fit_logistic_lasso

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre># simulte some data
</pre>
lambda &lt;- 0.3

# compute coefficients and intercept using glmnet and store as int_true and

# beta_true.

ret &lt;- fit_logistic_lasso(x=x,y=y,lambda = 0.3)

if (abs(int_true – ret$intercept) &gt; 0.01) { ## this may not be the tolerance! print(glue::glue(“Test failed. Expected intercept {int_true} but got

<pre>                  {ret$intercept}\n")
</pre>
}

if (mean(abs(beta_true – ret$beta)) &gt; 0.01) { ## this may not be the tolerance! print(glue::glue(“Test failed. Expected computed beta had an error of

</div>
</div>
<div class="layoutArea">
<div class="column">
}

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>{mean(abs(beta_true - ret$beta))}.\n")
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
The unit tests will test both functions and will test the tidymodels interface.

I strongly recommend that you write your own version of these tests to check your code. This is a situation where you can (and should!) collaborate with fellow students and compare your test code. As always, you are not allowed to collaborate on any other aspect of this assignment.

Which packages can you use

You can use any packages included when you run the following commands:

Note these are metapackages that include a whole host of other packages including dplyr, ggplot, and parsnip among others.

</div>
</div>
<div class="layoutArea">
<div class="column">
library(tidyverse) library(tidymodels)

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
In particular, you may not use any implementations of the logistic lasso in your submitted code (eg you can’t use the one in glmnet.). You may, however, find these implementations useful when you write your own tests. But please don’t submit this work.

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>

---
layout: post
title: Data Science Skills
---

The problem with Data Science these days is that nobody seems to agree on what it really is. [Wikipedia](https://en.wikipedia.org/wiki/Data_science) generously calls it "interdisciplinary"; a quick search on LinkedIn reveals job scopes that vary from `Analyst` roles to `Deep Learning`.

If you're new to Data Science, it feels especially daunting: *why does it seem as though there is an infinite number of skills to pick up*? 

Here, I try to give my own perspective of this, and some core skills to pick up (as well as frameworks).

----

# Core Skill #1: Wrangling with Data

No matter which company you are in, you never run away from data wrangling (i.e. doing things to data), which will occupy a lot of your time. The truth is that if you're supposed to do Data Science/Machine Learning, you can't not play with data.

- Specific Skill Tasks:
    - Data I/O (how do you load data? Save data?)
        - Subskills:
            - streaming data
            - large data files
            - multiple different data formats besides `csv`, including `(nd)json`, `hdf5` and `parquet`
    - Data reshaping (how do you modify data?)
        - Subskills:
            - Joins
            - Pivot tables (wide-to-long, `melt`/`reshape`)
    - Data Types (what are the core data types?)
        - Datetime handling
            - Datetime formats (string and timestamp)
            - Timezones
        - String handling
            - Regular Expressions
        - Numeric handling
            - Numeric types and their differences
        - Categories
    - Selecting Data (how do you pick the data you want?)
    - Handling missing data (how do you deal with missing data?)
    - Creating new data (how do you create new columns?)
- Frameworks/packages for different languages:
    - Python: 
        - [`pandas`](https://pandas.pydata.org/pandas-docs/stable/) is the most common framework for data wrangling. 
        - [`pyarrow`](https://arrow.apache.org/docs/python/) is a helpful "add-on" to `pandas` for managing large-scale data, particularly when reading/loading data. Wes McKinney, author of both `pandas` and Apache Arrow, documents his thoughts [here](https://wesmckinney.com/blog/apache-arrow-pandas-internals/), which makes for really insightful reading. 
        - [`pyspark`](https://www.numpy.org/) is the Python version of Spark. It deals very well with *very* large data, and that in itself is a skill that I can talk about separately.
   
    - R:
        - [`dplyr`](https://dplyr.tidyverse.org/), along with many other `tidyverse` libraries (written by Hadley Wickham), are very very useful in data manipulation. As a resource, I highly recommend [Hadley's own book on Data Science in R](https://r4ds.had.co.nz/).
    - SQL
        - To be fair, I think that SQL in itself is a very tricky thing to get into. I'll write more about SQL in upcoming posts
        
# Core Skill #2: Statistics and Probability

The first core skill was all about having the correct technical tools to take care of your subject matter (data). This skill is about learning how to understand what your subject matter is saying (statistics).

Unfortunately, statistics is [generally very badly taught](https://www.quora.com/Is-statistics-poorly-taught-and-explained-in-traditional-learning-institutions) in schools, because teachers focus more on how to use what statistical tests instead of why the tests even exist. As such, many of us lack the depth of understanding about Statistics as a discipline.

A good book recommendation to mitigate that is [Computer Age Statistical Inference](https://web.stanford.edu/~hastie/CASI/), which gives you the "why" along with the "how" -- and I don't necessarily mean the mathematical derivation. 

Anyhow, depending on what role you are in, your required knowledge of statistics can vary from "counting and basic probability" to really difficult stuff such as Markov chain Monte Carlo (MCMC). Like any other discipline, there's no end to the depth of Statistics you need to know, but these are some areas to consider:

- Probability:
    - Bayes' Rule and Conditional Probability
    - Probability Distributions
        - Examples (listing out the more popular ones):
            - Gaussian / Normal
            - Poisson
            - Bernoulli + Binomial
            - Exponential
            - Gamma
            - Beta
        - Properties
    - Random Variables
- Statistics:
    - Estimators (and estimating them)
    - Variance and Bias
    - Statistical Tests
    - Frequentism vs Bayesian
    - ANOVA
    - Time Series
    - Markov Processes
- Frameworks/packages for different languages:
    - Python:
        - `scipy` is the original Scientific Python package. A lot of really cool functionality is in here
        - `statsmodels` is a crossbreed of statistics with machine learning, and has functionality that reminds users of R
        - `numpy` technically is Numerical Python, and has a lot of the basic stuff (distributions)
    - R itself IS the framework. Built by statisticians, base R alone has a lot of stuff inside it that beats many other languages hands down.  

There is a lot more here that I'll expand in future posts.

# Core Skill #3: Machine Learning And Deep Learning

The third skill involves some level of mastery of the first two: now that you have the data, the means of handling the data, and the means of squeezing out some insight in the data, can you *create* some kind of crystal-ball to either understand the data better and/or predict the future?

Of course, some "data science" jobs need more of this than others; a deep-learning speech specialist will need to know a lot more about this than the average Data Scientist, and someone who does more analyst-style work will need less of this.

My recommendation for books for [machine learning (simpler](https://www-bcf.usc.edu/~gareth/ISL/ISLR%20Seventh%20Printing.pdf) and [more difficult)](https://web.stanford.edu/~hastie/Papers/ESLII.pdf) and [Deep Learning](https://github.com/janishar/mit-deep-learning-book-pdf) are all not "bedtime reading" books.

Here are some common algorithm families and key topics (I'll write on them)

- Supervised Learning
    - Decision Trees (includes Random Forests and XGBoost/AdaBoost)
    - Generalized Linear Models
    - Neural Nets
    - Some special use cases:
        - Recommender Systems
- Unsupervised Learning
    - Clustering Algorithms
- Explaining Decisions
- Metrics and key functions
    - Loss functions vs Metrics
    - Key functions:
        - ReLu
        - Softmax
- Optimization
    - Gradient Descent (and its various types)
- Principles across the discipline
    - Bias-Variance
    - Cross-Validation
    - Bootstrapping
    - Train/Test
    - Regularization
    - Required data-preprocessing
- Frameworks/packages for different languages:
    - Python:
        - `scikit-learn`, the main one for machine learning. It is a very comprehensive library, with some (very) minor drawbacks 
        - `tensorflow` and/or `keras` and/or `pytorch`, pick your poison for deep learning.
    - R: I cannot speak too much into a *unified* framework for R, because there really isn't one as far as I know.

# Side Skills

There are a host of side skills to pick up as part of a data scientist's skillset. These I have found less "necessary" depending on job posting, but they are not limited to the following:

- Data Visualization
- Data Engineering (Extract, Transform, Load)
- Backend programming

# credit-risk-replication

This pages has describes some  replication excercises in banking and credit risk modelling.

There is a [background reading page](background.md) with more references. 

Code source is on [Github](https://github.com/epogrebnyak/credit-risk-replication) 
and in notebooks in Google Colab.

## Why make these excercises?

It is a bit surprising there are so few open source numeric excercises with 
banking data and in credit risk modelling. 

Starting from more trivial   
excercises that focus on key relationships and computation tasks 
and going to more realistic portfolios and bank balance sheet detail can be 
a very fulfilling path, where a learner progressively gains confidence.

Yet there are obstacles: 

- lack of accessible textbooks (a lot of textbooks go deep into math too soon)
- lack of data, especially for corporate portfolios 
- general propensity for complex models that may obfuscate risk instead of revealing it
- bank risk management failure in 2008 
- plenty of noise in low-quality tutorials where machine learning would do all the necessary job.

What would I like to cover in these excercises? A starting point could be a bank with 
a portfolio of 100 identical loans with known probabilities of default. 
What amount of capital should a bank hold for these loans? What is the bank profit 
after a year of operation? What should the bank do next?  

From this starting point one can go into more assymetries:

- portfolio of loans of different sizes and credit quality
- household vs corporate loans
- more bank products (credit facility, guarantees)
- what happens at default
- single bank vs bank system view in broader economy
- bank in a business cycke

It would be nice to provide small pieces fo data and code to show that 
you can build up you understanding of empirical banking 
and credit risk incrementally. Below are some starter excercises in this direction.

## Excercise 1: Simulate empirical default probability distributions

Replicate [IMF 2006. Review and Implementation of Credit Risk Models of the Financial Sector
Assessment Program](https://www.imf.org/external/pubs/ft/wp/2006/wp06134.pdf).

#### Pipeline:

- We start with indepndent defaults and then move to dependent defaults
- We simulate defaults in a given loan portfolio with known PD
- We plot empiric default probability density functions
- We calculate expected and unexpected loss

#### Code:

[![](https://badgen.net/badge/colab/loss_density.ipynb/orange)][colab_1]

[colab_1]: https://colab.research.google.com/drive/1xJCGGFTVd6hPqa2F_v5VwXwsU5qlNIi5?usp=sharing

#### Takeaway:

Your choice of modelling technique affects your estimate of portfolio riskiness,
for example dependent defaults increase porfolio risk.

#### Used dataset:

- CSFP

## Excercise 2: roll forward portfolio structure by credit quality grades

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">If a BBB loan becomes BB, capital requirements will increase and expected losses too. And this will impact CET1. So, you need to understand how the rating split (including default) will move over time. To do this, one uses rating transition matrices.</p>&mdash; JohannesBorgen (@jeuasommenulle) <a href="https://twitter.com/jeuasommenulle/status/1255122789960429572?ref_src=twsrc%5Etfw">April 28, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 


# Copyright

(C) 2021 Evgeniy Pogrebnyak and contributors

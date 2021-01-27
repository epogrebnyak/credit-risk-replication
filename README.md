# credit-risk-replication

This is a [background reading](background.md)
and several replication excercises in credit risk modelling.


# Excercises

## Excercise 1: Simulate default probability distributions

Replicate [IMF 2006. Review and Implementation of Credit Risk Models of the Financial Sector
Assessment Program](https://www.imf.org/external/pubs/ft/wp/2006/wp06134.pdf).

Pipeline:

- We start with indepndent defaults and then move to dependent defaults
- We simulate defaults in a given loan portfolio with known PD
- We plot empiric default probability density functions
- We calculate expected and unexpected loss

Code:

[loss_density.ipynb](https://colab.research.google.com/drive/1xJCGGFTVd6hPqa2F_v5VwXwsU5qlNIi5#scrollTo=UWg1dhYasQQx)

Takeaway:

Your choice of modelling technique affects your estimate of portfolio riskiness,
for example dependent defaults increase porfolio risk.

Used dataset:

- CSFB 

## Excercise 2: roll forward portfolio structure by credit quality grades

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">If a BBB loan becomes BB, capital requirements will increase and expected losses too. And this will impact CET1. So, you need to understand how the rating split (including default) will move over time. To do this, one uses rating transition matrices.</p>&mdash; JohannesBorgen (@jeuasommenulle) <a href="https://twitter.com/jeuasommenulle/status/1255122789960429572?ref_src=twsrc%5Etfw">April 28, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

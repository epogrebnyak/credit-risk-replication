# credit-risk-replication

This is a [background reading](#background)
and [replication excercises](#excercises)
in credit risk modelling.

# Background

## Concepts

Credit risk modelling goals:

- pricing of loans and bonds
- portfolio quality assessment and capital requirements
 
Modelling defaults: 

- a firm defaults when net asset price is negative ("structural" model, Merton)
- we just count observed defaults among similar groups of firms ("reduced" model)

Expected loss absorbed by reserves and unexpected loss by economic capital.


#### Textbooks

- Bluhm, Overbeck, and Wagner (2010). Introduction to Credit Risk Modeling. 

#### Papers and reviews

- [Bank of England (2015). Modelling Credit Risk](https://www.bankofengland.co.uk/-/media/boe/files/ccbs/resources/modelling-credit-risk)
- [Regulatory Capital Modelling for Credit Risk - Marek Rutkowski and Silvio Tarca (2016)](https://arxiv.org/pdf/1412.1183.pdf)

## Glossary

- PD
- LGD
- EAD

- ASRF

<!--

# People

- [Alan Matz](http://www.columbia.edu/~amm26/index.html)

# Courses

- http://dse.univr.it/safe/index.php?option=com_content&task=view&id=68&Itemid=91
- http://pages.stern.nyu.edu/~sternfin/vacharya/public_html/091-b403305-acharya.pdf


# More

- https://www.fdic.gov/analysis/cfr/working-papers/2009/2009-10.pdf
- http://pages.stern.nyu.edu/~sternfin/vacharya/public_html/091-b403305-acharya.pdf

# Quotes 

More references:

- [The Vasicek model is the same as the intensity model with a Gaussian copula, identical default
probabilities and a large number of names.](http://dse.univr.it/safe/documents/SSEFCANAZEI2012/07_correlation_-_modeling.pdf)
- [Caution over Copulas: Gaussian copula (method described here) widely used in practice but quite possibly a poor description of reality.```](http://leonardo3.dse.univr.it/safe/documents/SSEFCANAZEI2012/06_the_default_intensity_model_and_the_copula_approach.pdf)

-->

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

## Excercise 2: roll forward portfolio structure by grades

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">If a BBB loan becomes BB, capital requirements will increase and expected losses too. And this will impact CET1. So, you need to understand how the rating split (including default) will move over time. To do this, one uses rating transition matrices.</p>&mdash; JohannesBorgen (@jeuasommenulle) <a href="https://twitter.com/jeuasommenulle/status/1255122789960429572?ref_src=twsrc%5Etfw">April 28, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

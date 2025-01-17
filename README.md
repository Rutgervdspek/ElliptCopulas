Package ElliptCopulas
=====================


This package implements several functions for the estimation of meta-elliptical copulas and for the estimation of elliptical and trans-elliptical distributions:

* *elliptical distributions* are distributions for which the isodensity surfaces/curves are ellipses. Their distribution is determined by a mean, a variance matrix and a univariate function called the generator.

* *(meta-)elliptical copulas* are copulas defined implicitly as copula functions of elliptical distributions. Their distribution is determined by a correlation matrix and a generator.

* *trans-elliptical distributions* are distributions whose copula is meta-elliptical and whose margins are arbitrary. In other words, a trans-elliptical distribution is a multivariate distribution built from the dependence structure (copula) of an elliptical distribution, but which could have any margin. Their distribution is therefore determined by the marginal distributions, the correlation matrix and the generator.



# How to install

The release version on CRAN:

```r
install.packages("ElliptCopulas")
```

The development version from GitHub:

```r
# install.packages("remotes")
remotes::install_github("AlexisDerumigny/ElliptCopulas")
```

# Main functions of the package

**Inference of Elliptical Distributions**

* `EllDistrEst`: nonparametric estimation of the generator of an elliptical distribution.

* `EllDistrSim`: simulate data from an elliptical distribution with a given arbitrary generator.


**Inference of (Meta-)Elliptical Copulas**

* `EllCopEst`: nonparametric estimation of the generator of an elliptical copula.

* `EllCopSim`: simulate data from an elliptical copula with a given arbitrary generator.

* `EllCopLikelihood`: compute the likelihood of a given elliptical copula generator.


**Inference of Trans-Elliptical Distributions**

* `TEllDistrEst`: estimation of the marginal cdfs, estimation of the correlation matrix by inversion of Kendall's tau and nonparametric estimation of the generator.


**Numerical analysis**

* `DensityGenerator.normalize`: normalize an elliptical copula density generator in order to satisfy the identifiability constraints.

* `DensityGenerator.check`: check whether a given density generator is normalized.

* `Convert_gd_To_g1`, `Convert_g1_To_Fg1`, `Convert_g1_To_Qg1`, `Convert_g1_To_f1`, `Convert_gd_To_fR2`:
convert between
  * a d-dimensional generator gd
  * the 1-dimensional version g1
  * the density f1 of a 1 dimensional margin
  * the cdf Fg1 of a 1-dimensional margin
  * the quantile function Qg1 of a 1-dimensional margin
  * the density fR2 of the random variable R^2, where X = RV, with R the modular variable of X, V uniform on the d-dimensional unit sphere, and X is an elliptically distributed random vector.


# References

Derumigny, A., & Fermanian, J. D. (2021). Identifiability and estimation of meta-elliptical copula generators. ArXiv preprint, [arXiv:2106.12367](https://arxiv.org/pdf/2106.12367.pdf).

Liebscher, E. (2005). A semiparametric density estimator based on elliptical distributions, Journal of Multivariate Analysis, 92, 205–225. [doi:10.1016/j.jmva.2003.09.007](https://doi.org/10.1016/j.jmva.2003.09.007)


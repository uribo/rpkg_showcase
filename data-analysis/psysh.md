

# psych: Procedures for Psychological, Psychometric, and Personality Research

心理学研究のための手法に関するパッケージ

[![](http://www.r-pkg.org/badges/version/psych)](http://cran.rstudio.com/web/packages/psych/index.html)

* CRAN: http://cran.r-project.org/web/packages/psych/index.html
* URL: http://personality-project.org/r/psych


```r
> library(psych)
```

```

Attaching package: 'psych'

The following object is masked from 'package:grofit':

    logistic

The following object is masked from 'package:geiger':

    rescale

The following object is masked from 'package:Hmisc':

    describe

The following objects are masked from 'package:ggplot2':

    %+%, alpha
```

バージョン: 1.5.6

-----



| 関数名 | 概略 |
|--------|------|
| `Bechtoldt` | Seven data sets showing a bifactor solution. 
| `Dwyer` | 8 cognitive variables used by Dwyer for an example. |
| `Gleser` | Example data from Gleser, Cronbach and Rajaratnam (1965) to show basic principles of generalizability theory. |
| `Gorsuch` | Example data set from Gorsuch (1997) for an example factor extension. |
| `Harman` | Two data sets from Harman (1967). 9 cognitive variables from Holzinger and 8 emotional variables from Burt |
| `Harman.5` | 5 socio-economic variables from Harman (1967) |
| `Harman.8` | Correlations of eight physical variables (from Harman, 1966) |
| `Harman.political` | Eight political variables used by Harman (1967) as example 8.17 |
| `ICC` | Intraclass Correlations (ICC1, ICC2, ICC3 from Shrout and Fleiss) |
| `ICLUST.cluster` | Function to form hierarchical cluster analysis of items |
| `ICLUST.graph` | create control code for ICLUST graphical output |
| `ICLUST.rgraph` | Draw an ICLUST graph using the Rgraphviz package |
| `ICLUST.sort` | Sort items by absolute size of cluster loadings |
| `KMO` | Find the Kaiser, Meyer, Olkin Measure of Sampling Adequacy |
| `Promax` | Perform bifactor, promax or targeted rotations and return the inter factor angles. |
| `SD` | Find the Standard deviation for a vector, matrix, or data.frame - do not return error if there are no cases |
| `Schmid` | 12 variables created by Schmid and Leiman to show the Schmid-Leiman Transformation |
| `Tucker` | 9 Cognitive variables discussed by Tucker and Lewis (1973) |
| `VSS` | Apply the Very Simple Structure, MAP, and other criteria to determine the appropriate number of factors. |
| `VSS.parallel` | Compare real and random VSS solutions |
| `VSS.plot` | Plot VSS fits |
| `VSS.scree` | Plot the successive eigen values for a scree test |
| `Yule` | From a two by two table, find the Yule coefficients of association, convert to phi, or tetrachoric, recreate table the table to create the Yule coefficient. |
| `ability` | 16 ability items scored as correct or incorrect. |
| `affect` | Two data sets of affect and arousal scores as a function of personality and movie conditions |
| `alpha` | Find two estimates of reliability: Cronbach's alpha and Guttman's Lambda 6. |
| `bestScales` | A set of functions for factorial and empirical scale construction |
| `bfi` | 25 Personality items representing 5 factors |
| `bi.bars` | Draw pairs of bargraphs based on two groups |
| `biplot.psych` | Draw biplots of factor or component scores by factor or component loadings |
| `block.random` | Create a block randomized structure for n independent variables |
| `blot` | Bond's Logical Operations Test - BLOT |
| `bock` | Bock and Liberman (1970) data set of 1000 observations of the LSAT |
| `burt` | 11 emotional variables from Burt (1915) |
| `circ.tests` | Apply four tests of circumplex versus simple structure |
| `cities` | Distances between 11 US cities |
| `cluster.fit` | cluster Fit: fit of the cluster model to a correlation matrix |
| `cluster.loadings` | Find item by cluster correlations, corrected for overlap and reliability |
| `cluster.plot` | Plot factor/cluster loadings and assign items to clusters by their highest loading. |
| `cluster2keys` | Convert a cluster vector (from e.g., kmeans) to a keys matrix suitable for scoring item clusters. |
| `cohen.kappa` | Find Cohen's kappa and weighted kappa coefficients for correlation of two raters |
| `comorbidity` | Convert base rates of two diagnoses and their comorbidity into phi, Yule, and tetrachorics |
| `cor.ci` | Bootstrapped confidence intervals for raw and composite correlations |
| `cor.plot` | Create an image plot for a correlation or factor matrix |
| `cor.smooth` | Smooth a non-positive definite correlation matrix to make it positive definite |
| `cor.wt` | The sample size weighted correlation may be used in correlating aggregated data |
| `cor2dist` | Convert correlations to distances (necessary to do multidimensional scaling of correlation data) |
| `corFiml` | Find a Full Information Maximum Likelihood (FIML) correlation or covariance matrix from a data matrix with missing data |
| `corr.test` | Find the correlations, sample sizes, and probability values between elements of a matrix or data.frame. |
| `correct.cor` | Find dis-attenuated correlations given correlations and reliabilities |
| `cortest.bartlett` | Bartlett's test that a correlation matrix is an identity matrix |
| `cortest.mat` | Chi square tests of whether a single matrix is an identity matrix, or a pair of matrices are equal. |
| `cosinor` | Functions for analysis of circadian or diurnal data |
| `count.pairwise` | Count number of pairwise cases for a data set with missing (NA) data. |
| `cta` | Simulate the C(ues) T(endency) A(ction) model of motivation |
| `cubits` | Galton's example of the relationship between height and 'cubit' or forearm length |
| `cushny` | A data set from Cushny and Peebles (1905) on the effect of three drugs on hours of sleep, used by Student (1908) |
| `densityBy` | Create a 'violin plot' or density plot of the distribution of a set of variables |
| `describe` | Basic descriptive statistics useful for psychometrics |
| `describeBy` | Basic summary statistics by group |
| `df2latex` | Convert a data frame, correlation matrix, or factor analysis output to a LaTeX table |
| `diagram` | Helper functions for drawing path model diagrams |
| `draw.tetra` | Draw a correlation ellipse and two normal curves to demonstrate tetrachoric correlation |
| `dummy.code` | Create dummy coded variables |
| `eigen.loadings` | Convert eigen vectors and eigen values to the more normal (for psychologists) component loadings |
| `ellipses` | Plot data and 1 and 2 sigma correlation ellipses |
| `epi` | Eysenck Personality Inventory (EPI) data for 3570 participants |
| `epi.bfi` | 13 personality scales from the Eysenck Personality Inventory and Big 5 inventory |
| `error.bars` | Plot means and confidence intervals |
| `error.bars.by` | Plot means and confidence intervals for multiple groups |
| `error.crosses` | Plot x and y error bars |
| `errorCircles` | Two way plots of means, error bars, and sample sizes |
| `fa` | Exploratory Factor analysis using MinRes (minimum residual) as well as EFA by Principal Axis, Weighted Least Squares or Maximum Likelihood |
| `fa.diagram` | Graph factor loading matrices |
| `fa.extension` | Apply Dwyer's factor extension to find factor loadings for extended variables |
| `fa.parallel` | Scree plots of data or correlation matrix compared to random "parallel" matrices |
| `fa.sort` | Sort factor analysis or principal components analysis loadings |
| `factor.congruence` | Coefficient of factor congruence |
| `factor.fit` | How well does the factor model fit a correlation matrix. Part of the VSS package |
| `factor.model` | Find R = F F' + U2 is the basic factor model |
| `factor.residuals` | R* = R- F F' |
| `factor.rotate` | "Hand" rotate a factor loading matrix |
| `factor.scores` | Various ways to estimate factor scores for the factor analysis model |
| `factor.stats` | Find various goodness of fit statistics for factor analysis and principal components |
| `factor2cluster` | Extract cluster definitions from factor loadings |
| `fisherz` | Fisher r to z and z to r and confidence intervals |
| `galton` | Galton's Mid parent child height data |
| `geometric.mean` | Find the geometric mean of a vector or columns of a data.frame. |
| `glb.algebraic` | Find the greatest lower bound to reliability. |
| `harmonic.mean` | Find the harmonic mean of a vector, matrix, or columns of a data.frame |
| `headTail` | Combine calls to head and tail |
| `heights` | A data.frame of the Galton (1888) height and cubit data set. |
| `iclust` | iclust: Item Cluster Analysis - Hierarchical cluster analysis using psychometric principles |
| `iclust.diagram` | Draw an ICLUST hierarchical cluster structure diagram |
| `income` | US family income from US census 2008 |
| `interp.median` | Find the interpolated sample median, quartiles, or specific quantiles for a vector, matrix, or data frame |
| `iqitems` | 16 multiple choice IQ items |
| `irt.1p` | Item Response Theory estimate of theta (ability) using a Rasch (like) model |
| `irt.fa` | Item Response Analysis by Exploratory Factor Analysis of tetrachoric/polychoric correlations |
| `irt.item.diff.rasch` | Simple function to estimate item difficulties using IRT concepts |
| `irt.responses` | Plot probability of multiple choice responses as a function of a latent trait |
| `kaiser` | Apply the Kaiser normalization when rotating factors |
| `logistic` | Logistic transform from x to p and logit transform from p to x |
| `lowerUpper` | Combine two square matrices to have a lower off diagonal for one, upper off diagonal for the other |
| `make.keys` | Create a keys matrix for use by score.items or cluster.cor |
| `mardia` | Calculate univariate or multivariate (Mardia's test) skew and kurtosis for a vector, matrix, or data.frame |
| `mat.sort` | Sort the elements of a correlation matrix to reflect factor loadings |
| `matrix.addition` | A function to add two vectors or matrices |
| `mediate` | Estimate and display direct and indirect effects of mediators and moderator in path models |
| `mixed.cor` | Find correlations for mixtures of continuous, polytomous, and dichotomous variables |
| `msq` | 75 mood items from the Motivational State Questionnaire for 3896 participants |
| `mssd` | Find von Neuman's Mean Square of Successive Differences |
| `multi.hist` | Multiple histograms with density and normal fits on one page |
| `neo` | NEO correlation matrix from the NEO_PI_R manual |
| `omega` | Calculate McDonald's omega estimates of general and total factor saturation |
| `omega.graph` | Graph hierarchical factor structures |
| `outlier` | Find and graph Mahalanobis squared distances to detect outliers |
| `p.rep` | Find the probability of replication for an F, t, or r and estimate effect size |
| `paired.r` | Test the difference between (un)paired correlations |
| `pairs.panels` | SPLOM, histograms and correlations for a data matrix |
| `parcels` | Find miniscales (parcels) of size 2 or 3 from a set of items |
| `partial.r` | Find the partial correlations for a set (x) of variables with set (y) removed. |
| `peas` | Galton's Peas |
| `phi` | Find the phi coefficient of correlation between two dichotomous variables |
| `phi.demo` | A simple demonstration of the Pearson, phi, and polychoric corelation |
| `phi2tetra` | Convert a phi coefficient to a tetrachoric correlation |
| `plot.psych` | Plotting functions for the psych package of class "psych" |
| `polar` | Convert Cartesian factor loadings into polar coordinates |
| `polychor.matrix` | Phi or Yule coefficient matrix to polychoric coefficient matrix |
| `predict.psych` | Prediction function for factor analysis or principal components |
| `principal` | Principal components analysis (PCA) |
| `print.psych` | Print and summary functions for the psych class |
| `psych` | A package for personality, psychometric, and psychological research |
| `psych.misc` | Miscellaneous helper functions for the psych package |
| `r.test` | Tests of significance for correlations |
| `rangeCorrection` | Correct correlations for restriction of range. (Thorndike Case 2) |
| `read.clipboard` | shortcut for reading from the clipboard |
| `rescale` | Function to convert scores to "conventional " metrics |
| `residuals.psych` | Extract residuals from various psych objects |
| `reverse.code` | Reverse the coding of selected items prior to scale analysis |
| `sat.act` | 3 Measures of ability: SATV, SATQ, ACT |
| `scaling.fits` | Test the adequacy of simple choice, logistic, or Thurstonian scaling. |
| `scatter.hist` | Draw a scatter plot with associated X and Y histograms, densitie and correlation |
| `schmid` | Apply the Schmid Leiman transformation to a correlation matrix |
| `score.alpha` | Score scales and find Cronbach's alpha as well as associated statistics |
| `score.irt` | Find Item Response Theory (IRT) based scores for dichotomous or polytomous items |
| `score.multiple.choice` | Score multiple choice items and provide basic test statistics |
| `scoreItems` | Score item composite scales and find Cronbach's alpha, Guttman lambda 6 and item whole correlations |
| `scoreOverlap` | Find correlations of composite variables (corrected for overlap) from a larger matrix. |
| `scrub` | A utility for basic data cleaning and recoding. Changes values outside of minimum and maximum limits to NA. |
| `setCor` | Set Correlation and Multiple Regression from matrix or raw input |
| `sim` | Functions to simulate psychological/psychometric data. |
| `sim.VSS` | create VSS like data |
| `sim.anova` | Simulate a 3 way balanced ANOVA or linear model, with or without repeated measures. |
| `sim.congeneric` | Simulate a congeneric data set |
| `sim.hierarchical` | Create a population or sample correlation matrix, perhaps with hierarchical structure. |
| `sim.item` | Generate simulated data structures for circumplex, spherical, or simple structure |
| `sim.multilevel` | Simulate multilevel data with specified within group and between group correlations |
| `sim.structure` | Create correlation matrices or data matrices with a particular measurement and structural model |
| `simulation.circ` | Simulations of circumplex and simple structure |
| `smc` | Find the Squared Multiple Correlation (SMC) of each variable with the remaining variables in a matrix |
| `spider` | Make "radar" or "spider" plots. |
| `splitHalf` | Alternative estimates of test reliabiity |
| `statsBy` | Find statistics (including correlations) within and between groups for basic multilevel analyses |
| `structure.diagram` | Draw a structural equation model specified by two measurement models and a structural model |
| `structure.list` | Create factor model matrices from an input list |
| `superMatrix` | Form a super matrix from two sub matrices. |
| `table2matrix` | Convert a table with counts to a matrix or data.frame representing those counts. |
| `test.psych` | Testing of functions in the psych package |
| `tetrachoric` | Tetrachoric, polychoric, biserial and polyserial correlations from various types of input |
| `thurstone` | Thurstone Case V scaling |
| `tr` | Find the trace of a square matrix |
| `vegetables` | Paired comparison of preferences for 9 vegetables |
| `winsor` | Find the Winsorized scores, means, sds or variances for a vector, matrix, or data.frame |
| `withinBetween` | An example of the distinction between within group and between group correlations |

-----

## scrub

特定の値をNAに置換する

## spider
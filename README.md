# Rh-TiO2-classificator

## Introduction

On the basis of the article “Rhodium nanoparticles impregnated on TiO2: strong morphological effects on hydrogen production” (https://doi.org/10.1039/D0NJ02419H) authored by B. L. Albuquerque, G. Chacón, M. Nazarkovsky and J. Dupont, data analysis of the size distribution profiles for all three subject samples of Rh-TiO2 was performed (the outliers’ analysis, distributions classification, analysis of variances, discriminant analysis). The Rh nanoparticles were characterized by different shapes – cuboctahedral (spherical) NP, cubic NC and octahedral Oh. The results allowed us to distinguish each shape type of the nanoparticles by their size distribution profiles from respective microphotographs and make predictive modeling by means of algorithms to classify them. To this end, machine learning approaches, such as Naïve Bayes, Logistic Regression, K-Nearest Neighbors, Support Vector Machine and Decision Tree were trained, validated and compared by their effectiveness to predict the samples. The most effective model has turned out to be Logistic Regression, whose misclassification rate at the validation stage was less than 13% (12.82%) at the minimal mean -log(p) = 0.2509. As a result, an offline calculator to predict the samples type was developed and the prediction formula was provided. The project was coded by means of JSL (JMP Scripting Language, SAS).

## Methods for the analysis of variances

For adequate distribution analysis the data preparation, the outliers were detected with the Malahanobis distances approach and the K-Nearest neighbors. 
The analysis of variances on the particles size by type (NP, NC or Oh) was undertaken using homo/heteroscedasticity comparison with the help of the Bryan-Forsythe, Bartlett, Levene and O’Brien tests, assuming the null hypothesis (Ho) that the variances are equal, but each uses a different method for measuring variability. Levene’s test estimates the mean value of these absolute differences for each group. Then, a t-test is conducted (or equivalently, an F-test) on these estimates. The Brown-Forsythe test measures the differences from the median instead of the mean (opposed to Levene’s test) and tests these differences. O’Brien’s test tricks the t-test by telling it that the means were really variances. Bartlett’s test derives the test mathematically, using an assumption that the data are normal. Despite its power, the subject test is not robust in respect to disnormality. 
For understanding the effect of size distribution, all three samples as three variances were subjected to study with the help of the of ANOVA F-test (in case of homoscedastic) or nonparametric Wilcoxon (known also as Whitney-Mann) test (in case of heteroscedastic). 
Additionally, the means comparison with the Tukey-Kramer HSD test was performed. The α-criterion of acceptance/reject of Ho is 0.05. 
For the future prediction, a series of machine learning models was set: Classification Tree, Naïve Bayes, Support Vector Machine, Logistic Regression, K-Nearest Neighbors. The models were compared by the set metrics for categorical responses, such as misclassification rate (MR), entropy of R2 and supported by the confusion matrices







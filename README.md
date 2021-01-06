# Rh-TiO2-classificator

#Introduction

On the basis of the article “Rhodium nanoparticles impregnated on TiO2: strong morphological effects on hydrogen production” (https://doi.org/10.1039/D0NJ02419H) authored by Brunno L. Albuquerque, Gustavo Chacón, Michael Nazarkovsky and  Jairton Dupont, data analysis of the size distribution profiles for all three subject samples (NP, NC and Oh) was performed (outliers analysis, distributions classification, analysis of variances, discriminant analysis). The results allowed us to distinguish each type of the samples by their size distribution profiles and make predictive modeling for the algorithms to classify them. To this end, machine learning approaches, such as Naive Bayes, Logistic Regression, K-Nearest Neighbors, Discriminant Analysis, Support Vector Machine and Decision Tree were trained, validated and compared by their effectiveness to predict the samples. The most effective model has turned out to be Logistic Regression, whose misclassification rate at the validation stage of the model is less than 13% (12.81%) at the minimal mean -log(p) = 0.2509. As a result, an offline calculator to predict the samples type was developed and the prediction formula was provided. The project was coded by means of JSL (JMP Scripting Language, SAS).

##Methods for the analysis of variances

The analysis of variances on the particles size by type (NP, NC or Oh) was undertaken using homo-heteroscedasticity comparison with the Bryan-Forsythe, Bartlett, Levene and O’Brien tests, assuming the null hypothesis that the variances are equal, but each uses a different method for measuring variability:
• Levene’s test estimates the mean value of these absolute differences for each group. Then, a t-test is conducted (or equivalently, an F-test) on these estimates.
• The Brown-Forsythe test measures the differences from the median instead of the mean (opposed to Levene’s test) and tests these differences.
• O’Brien’s test tricks the t-test by telling it that the means were really variances.
• Bartlett’s test derives the test mathematically, using an assumption that the data are normal. Despite its power, the subject test is not robust in respect to disnormality. 






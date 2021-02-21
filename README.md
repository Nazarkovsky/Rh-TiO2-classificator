# Rh-TiO2-classificator

## Introduction

On the basis of the article “Rhodium nanoparticles impregnated on TiO2: strong morphological effects on hydrogen production” (https://doi.org/10.1039/D0NJ02419H) authored by B. Albuquerque, G. Chacón, M. Nazarkovsky and J. Dupont data analysis of the size distribution profiles for all three subject samples (NP, NC and Oh) was performed (distributions classification, analysis of variances, discriminant analysis). The samples feature in different shape of Rh nanoparticles (NP – spherical, NC – cubic, Oh - octahedral) and, as a result, their photocatalytic activity was proven to be dependent on the morphology. The results allowed us to distinguish the types of the samples by their profiles and make predictive modeling for the machine learning algorithms to classify the samples by their particles size distributions. The developed algorithms can be deployed and serve for identification of the sample from TEM images. To this end, machine learning approaches, such as non-parametric K-Nearest Neighbors approach (maximal K = 100, metrics: Euclidean distance at the uniform weight), Naïve Bayes, Logistic Regression, Bootstrap Forest (1 split per sample, learning rate 0.1, 35 trees) and Classification Tree (9 splits) were trained, validated and their effectiveness to predict the samples by their size distribution profiles was compared. The learning rate at 0.1 is recommended in order to avoid overfitting the real experimental data. The most effective model has turned out to be Logistic Regression, whose error, misclassification rate (MR), at the validation stage is less than 8% (7.64%). This model’s other metrics – Generalized R2, Entropy R2 – are the highest, as compared to the models at the same MR (Naïve Bayes and Bootstrap Forest). As a result, an offline calculator for Logistic Regression was developed and provided on github.com to predict the samples type. The project was coded by means of JSL (SAS).

A short communication with discussions is available on LinkedIn: https://www.linkedin.com/pulse/data-science-chemical-v-tem-images-based-predictive-rh-nazarkovsky









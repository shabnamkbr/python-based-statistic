# python-based-statistic
Statistical analysis scripts used in the associated research project
IQ Statistical Analysis in Python

This repository contains a simple Python workflow for performing statistical analyses on an IQ dataset stored in an Excel file. The project demonstrates how to read Excel data using Pandas and apply common statistical tests using SciPy.

## Overview

The analysis includes:

Checking whether FSIQ scores follow a normal distribution using the Shapiro–Wilk test.

Comparing FSIQ scores between males and females using an independent samples t-test.

Inspecting missing values and basic information for the Age and FSIQ variables.

Evaluating the relationship between Age and FSIQ using Pearson correlation.

Creating High and Low IQ groups based on the median FSIQ score.

Testing the association between Gender and IQ group using the Chi-square test of independence.

Comparing the ages of participants in the High and Low IQ groups using another independent samples t-test.

## Dataset

The Excel file should contain at least the following columns:

FSIQ: Full Scale IQ score

Gender: Participant gender (M or F)

Age: Participant age


## Statistical Methods

1. Shapiro–Wilk Test

Tests whether the FSIQ variable is normally distributed.

2. Independent Samples t-Test

Compares the mean FSIQ scores of male and female participants.

3. Pearson Correlation

Measures the linear relationship between Age and FSIQ.

4. Chi-Square Test of Independence

Examines whether IQ group (High/Low) is associated with Gender.

5. Independent Samples t-Test for Age

Compares the ages of participants in the High and Low IQ groups.


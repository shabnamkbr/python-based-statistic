python-based-statistic

Statistical analysis scripts used in the associated research project IQ Statistical Analysis in Python.

This repository contains Python scripts for performing descriptive and inferential statistical analyses on an IQ dataset stored in an Excel file. The workflow automatically checks statistical assumptions and selects the appropriate statistical test based on the characteristics of the data.

Features

The scripts perform the following analyses:

Read participant data from an Excel file using Pandas.
Display basic information and check for missing values.
Visualize FSIQ distribution using a Boxplot.
Test normality using the Shapiro–Wilk test.
Compare FSIQ scores between males and females.
Automatically choose between:
Independent Samples t-test
Welch's t-test
Mann–Whitney U test
Calculate Cohen's d as the effect size for group comparisons.
Evaluate the relationship between Age and FSIQ.
Automatically choose between:
Pearson correlation
Spearman rank correlation
Test the association between Gender and IQ class (Low vs High).
Automatically choose between:
Chi-square test of independence
Fisher's Exact test (when Chi-square assumptions are violated)
Calculate Cramer's V as the effect size for Chi-square analyses.
Compare participant age between Low and High IQ groups using the appropriate statistical test.
Dataset

The Excel dataset should contain at least the following columns:

Column	Description
FSIQ	Full Scale IQ score
Gender	Participant gender (M/F)
Age	Participant age
class	IQ classification (Low, Average, High)

The scripts use only the Low and High IQ classes for group-comparison analyses. Participants classified as Average are excluded from those specific analyses.

Statistical Methods
Shapiro–Wilk Test

Evaluates whether continuous variables are approximately normally distributed.

If normality is violated, non-parametric methods are automatically selected.

Levene's Test

Evaluates equality of variances between two groups.

Equal variances → Independent Samples t-test
Unequal variances → Welch's t-test
Independent Samples t-Test

Compares the means of two independent groups when assumptions of normality are satisfied.

Welch's t-Test

Used instead of the standard t-test when group variances are unequal.

Mann–Whitney U Test

A non-parametric alternative to the independent samples t-test.

Used when normality assumptions are not met.

Pearson Correlation

Measures the linear relationship between Age and FSIQ when both variables are normally distributed.

Spearman Rank Correlation

Measures the monotonic relationship between Age and FSIQ when normality assumptions are violated.

Chi-Square Test of Independence

Evaluates whether Gender and IQ class are statistically associated.

Before performing the test, expected cell frequencies are checked.

Fisher's Exact Test

Automatically replaces the Chi-square test when expected cell frequencies are too small (typically < 5).

Effect Size
Cohen's d

Reports the magnitude of the difference between two independent groups.

Cramer's V

Reports the strength of association between categorical variables in Chi-square analyses.

Required Python Packages
pip install pandas
pip install scipy
pip install numpy
pip install matplotlib
pip install openpyxl

Or install everything at once:

pip install pandas scipy numpy matplotlib openpyxl
Running the Analysis
Place the Excel dataset in your desired directory.
Update the file path in the script
Run the Python script:
python main.py
Output

The scripts automatically report:

Sample sizes
Summary statistics
Normality assessment
Selected statistical test
Test statistic
p-value
Effect size (when applicable)
A plain-English interpretation of the results
Libraries Used
Pandas
NumPy
SciPy
Matplotlib
OpenPyXL

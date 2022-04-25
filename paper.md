---
title: 'ExploriPy : A Python Library for Pre-Modelling Data Analysis with EDA and Statistical Tests'
tags:
  - exploratory-data-analysis
  - statistical-tests
  - anova
  - exploratory-analysis
  - exploratory-data-visualization
authors:
  - name: Kunjithapatham Sivakumar^[Corresponding author] # note this makes a footnote saying 'Co-first author'
    orcid: 0000-0000-0000-0000
    affiliation: 1 
  - name:  Shashank Shekhar
    affiliation: 2
  - name: Sajan Bhagat
    affiliation: 3
  - name: Asif Salim
    affiliation: 4
affiliations:
 - name: Director - AI-Labs,Subex Ltd, Bangalore, India
   index: 1
 - name: Head, AI-Labs, Subex Ltd, Bangalore, India
   index: 2
 - name: Associate Director - AI Labs, Subex Ltd, Bangalore, India
   index: 3
 - name: Research Scientist - AI Labs, Subex Ltd, Bangalore, India
   index: 4
---
date: 20 April 2022
bibliography: paper.bib

# Summary

Exploratory Data Analysis (EDA) [@tukey1977exploratory]is one of the crucial steps in data science that facilitates generating insights and statistical measures which are essential for building predictive models. EDA is always a time-consuming activity and requires a thorough analysis of datasets to summarize their main characteristics. It is always required to do an initial analysis of the data, and then deep dive into further domain-specific analysis, based on the initial insights. Currently, there is no comprehensive library in Python, which could do the initial data analysis and statistical tests, and present an output, which could be easily interpreted and shared across the stakeholders. Though there are several individual packages available for statistical tests, interpretation of the output requires a certain level of statistical knowledge. In this package, we introduce an automated data analysis platform that performs a series of EDA processes and statistical tests. The results are rendered in the form of an HTML document including the visualization and relevant data download corresponding to the analysis steps. This makes ExploriPy an easy-to-use tool for the community which lacks in-depth statistical and EDA domain knowledge.

# Statement of need

ExploriPy reduces a data analyst’s efforts significantly in the initial EDA. It is designed in a way to perform automated EDA, and statistical tests including Analysis of Variance, Chi Square Test of Independence, Weight of Evidence, Information Value and Tukey Honest Significance Difference. It provides easy interpretation on these statistical test results based on industry standard assumptions. It expects a Pandas DataFrame along with a list of categorical variables, as input. Output will be a presentable HTML document with the result of analysis and statistical tests represented through several interactive charts, and tables (with option to download as CSV). The ExploriPy package is available in the Python Package Index.

# Key features

The important features of this library are listed below.

\begin{enumerate}
\item The input is taken in the form of Pandas dataframe along with an optional lists of categorical and continous features. There is in-built logic to automatically identify categorical features. A target variable has to be specified for analysis and statistical tests.
\item The output of the EDA is provided as an HTML page with a data download option corresponding to the analysis and tests.
\item A list of features and their data types are displayed.
\item A chart showing percentage of categorical, continuous and other variables.
\item A bar chart showing the percentage of null values in each feature.
\item General target variable information - total number of records, total number of nulls in the target, and percentage of nulls in the target. 
\begin{itemize}
\item For categorical target variable - list of categories and number of records for each category, and pie chart on percentage of categorical variables.
\item For continuous target variable - statistics and distribution on the continuous target variable.
\end{itemize}
\item Statistical Tests
\begin{itemize}
\item Chi-square test of independence - to test the independence of two categorical variables. The test is used when both the independent variable and the dependent variable are both categorical. 
\item ANOVA (Analysis of variance) - This test is done for a selected target variable and it is used for finding its most influencing and non-influencing input categorical variables.
\item PostHoc Test (Tukey HSD) - to get the categories with the similar distribution.
\end{itemize}
\end{enumerate}

# References

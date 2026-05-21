# Unemployment and Crime in Turbulent times - Panel Evidence from the US State Data 2006-2016 and the California County Data 2012-2017

## Authors:

This project was authored by:

* Syeda Naveera Fatima Rizvi (sr5752@nyu.edu)
* Tiffany Jiayi Sun (js11828@nyu.edu)
* Yingfan Yang (yy3620@nyu.edu)

The authors are students from the M.A Economics Program (Class of 2022) at the Graduate School of Arts and Sciences at New York University.

This project was prepared for the Special Project in Economic Research as our Final Semester Thesis for Professor Michel Leonard. 
The course aims to integrate material and tools taught throughout the M.A. program to address applied economic and policy problems.

Please refer to the Unemployment and Crime.pdf file for

* The detailed analysis and report 
* All tables and figures

Please refer to the Modelling.ipynb file for the code for the regressions and descriptive statistics. 
Please refer to the Visualizations.ipynb file for the code for the data visualizations.

**Note:** _Please note that the python notebooks contains the relevant source codes only. For comprehensive analysis and explanations, please refer to the **Final Report (Special Projects in Econ Research - Unemployment and Crime.pdf).**_

## Project Overview and Business Understanding

This applied paper attempts to investigate whether a potential relationship exists between unemployment and violent/property crime, and if so then to what extent? The analysis begins with the hypothesis that a positive one exists and uses a fixed effects technique to empirically test it. Separate panel regressions are run for both violent and property crime for all the US states during the 2006-2016 period and the counties in California in the 2012-2017 time frame. 

## Programming Languages and Tools used

This project uses a combination of Exploratory Data Analysis and Fixed Effects Panel OLS Linear Regression for the analysis. All code is in Python

## Data Understanding and Source

The independent variables in this analysis are the violent and property crime rates. This paper defines violent crime as a crime in which an offender or perpetrator employs (or threatens to) the use of harmful force upon the victim (e.g. murder, assault, rape, and assassination). This paper defines property crime as a crime involving private property. This includes crimes such burglary, larceny, theft, motor vehicle theft, arson, shoplifting, and vandalism. 

The paper analyzes crime on two different levels; at the state level and the county level. Data for the state level crime rates (both violent and property) was obtained  from the FBI- Uniform Crime Reporting Program. The state crime rates are crime cases per 100,000 residents. Data for the county level crime rates was sourced from the California Department of Justice. The county crime rates are crime cases per 1000 residents. 

The data used for this report has also been uploaded in the Data folder

## Modelling and Evaluation

This paper employs the fixed effects technique to evaluate the impact of unemployment on violent and property crime. The fixed effects technique is used as it offers the advantage of making the different states and counties comparable. This technique also assists in controlling for omitted variable bias by control for time-invariant unobserved variables (e.g Average precipitation in a region).

Throughout the analysis the 95% confidence interval is used to determine the statistical significance of  parameters. All of the regressions are linear and the goal of this analysis is to draw inferences and aid interpretation. 

A total of four fixed effects regressions (one for each level and type of crime combination) are used. The general equation for these regressions is shown below:

$$Crime_{it} = \alpha_i + \gamma_t + \beta_1 Unemployment_{it} + \beta_2 X_{it} + \epsilon_{it}$$

where i and t are indices for the US states/counties and year respectively. $$Crime_{it}$$ represents violent/property crime, i captures the cross sectional fixed effect, t captures a year fixed effect,  $$\beta_1$$ is the semi-elasticity of the crime rate to the unemployment rate and $$X_{it}$$ indicates all the control variables.

## Key Insights

The EDA found that from the end of 2008 to the end of 2014 the unemployment rate has remained higher than the overall average value of 6.8% (Figure 1 below). It attained an all time high of 10% in the last quarter of 2009. During the 2006-2016 period, unemployment has greatly varied and both positive (2007-late 2009) and negative (2010-2016) trends are observed. Crime rates, however, have mostly been following a general downward trend (See Figure 2). Post 2010- all three rates are moving down in the same direction. Hence it is worth studying whether empirical evidence can be found to prove a positive relationship between unemployment and the crime rates

![unemployment](https://github.com/snaveerafrizvi/Unemployment-and-Crime-Final-Project/blob/main/Figures/US_unemp.jpg)
![crime](https://github.com/snaveerafrizvi/Unemployment-and-Crime-Final-Project/blob/main/Figures/US_trend.jpg)


This project includes a total of 4 regressions and results from 3 of them reject the hypothesis of a positive relationship. Using a 95% confidence level throughout, this paper finds;

* For states the relationship is negative with both violent and property crime. A 1 unit increase in the unemployment rate is associated with a 5.6 unit decrease in the violent crime rate and a 16.9 unit decrease in the property crime one for states. 
* For counties the relationship is negative with violent crime and positive with property. A 1 unit increase in the unemployment rate is associated with a 9.2 unit decrease in the violent crime rate, and a 60.2 unit increase in the property crime one for counties.
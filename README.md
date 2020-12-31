## [Appendices] Interests and Exposure Revisited: Explaining Gender Attitudes in the U.S. 1973-2018

### Table of Contents 

0. [Notes, Software, and Dependencies](#0-notes-software-and-dependencies)

1. [Regression Tables](#1-regression-tables)  
	a. [Multivariate Regression Tables](#a-multivariate-regression-tables---interactive-tables-made-available-here)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. [Abortion Attitudes Multivariate Regression](#i-abortion-attitudes-multivariate-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. [Sexual Behavior Attitudes Multivariate Regression](#ii-sexual-behavior-attitudes-multivariate-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. [Gender Roles Attitudes Multivariate Regression](#iii-gender-roles-attitudes-multivariate-regression)    
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. [Family Responsibilities Attitudes Multivariate Regression](#iv-family-responsibilities-attitudes-multivariate-regression)    
	b. [Ordinal Logistic Regression Tables](#b-ordinal-logistic-regression-tables---interactive-tables-made-available-here)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. [Abortion Attitudes Ordinal Logistic Regression](#i-abortion-attitudes-ordinal-logistic-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. [Sexual Behavior Attitudes Ordinal Logistic Regression](#ii-sexual-behavior-attitudes-ordinal-logistic-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. [Gender Roles Attitudes Ordinal Logistic Regression](#iii-gender-roles-attitudes-ordinal-logistic-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. [Family Responsibilities Attitudes Ordinal Logistic Regression](#iv-family-responsibilities-attitudes-ordinal-logistic-regression)  
	c. [Bivariate Regression Tables](#c-bivariate-regression-tables---interactive-tables-made-available-here)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. [Abortion Attitudes Bivariate Regression](#i-abortion-attitudes-bivariate-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ii. [Sexual Behavior Attitudes Bivariate Regression](#ii-sexual-behavior-attitudes-bivariate-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iii. [Gender Roles Attitudes Bivariate Regression](#iii-gender-roles-attitudes-bivariate-regression)  
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv. [Family Responsibilities Attitudes Bivariate Regression](#iv-family-responsibilities-attitudes-bivariate-regression)  


2. [Gender Attitudes Over Time by Political Preference](#2-gender-attitudes-over-time-by-political-preference)  
	a. [Mean Abortion Attitudes by Political Preference](#a-mean-abortion-attitudes-by-political-preference)  
	b. [Standard Deviation of Abortion Attitudes by Political Preference](#b-standard-deviation-of-abortion-attitudes-by-political-preference)  
	c. [Mean Sexual Behavior by Political Preference](#c-mean-sexual-behavior-by-political-preference)  
	d. [Standard Deviation of Sexual Behavior by Political Preference](#d-standard-deviation-of-sexual-behavior-by-political-preference)  
	e. [Mean Gender Role Attitudes by Political Preference](#e-mean-gender-role-attitudes-by-political-preference)  
	f. [Standard Deviation of Gender Role Attitudes by Political Preference](#f-standard-deviation-of-gender-role-attitudes-by-political-preference)  
	g. [Mean Family Responsibilities Attitudes by Political Preference](#g-mean-family-responsibilities-attitudes-by-political-preference)  
	h. [Standard Deviation of Family Responsibilities by Political Preference](#h-standard-deviation-of-family-responsibilities-by-political-preference)   
	
3. [Gender Attitudes Over Time by Race](#3-gender-attitudes-over-time-by-race)  
	a. [Mean Abortion Attitudes by Race](#a-mean-abortion-attitudes-by-race)  
	b. [Standard Deviation of Abortion Attitudes by Race](#b-standard-deviation-of-abortion-attitudes-by-race)  
	c. [Mean Gender Role Attitudes by Race](#c-mean-gender-role-attitudes-by-race)  
	d. [Standard Deviation of Gender Role Attitudes by Race](#d-standard-deviation-of-gender-role-attitudes-by-race)  
	e. [Mean Family Responsibilities Attitudes by Race](#e-mean-family-responsibilities-attitudes-by-race)  
	f. [Standard Deviation of Family Responsibilities by Race](#f-standard-deviation-of-family-responsibilities-by-race)  
	g. [Mean Sexual Behavior by Race](#g-mean-sexual-behavior-by-race)  
	h. [Standard Deviation of Sexual Behavior by Race](#h-standard-deviation-of-sexual-behavior-by-race)  

4. [Dependent Variable Question Phrasing](#4-dependent-variable-question-phrasing)  
	a. [Abortion Attitudes Question Phrasing](#a-abortion-attitudes-question-phrasing)  
	b. [Sexual Behavior Attitudes Question Phrasing](#b-sexual-behavior-attitudes-question-phrasing)  
	c. [Gender Role Attitudes Question Phrasing](#c-gender-roles-attitudes-question-phrasing)  
	d. [Family Responsibilities Attitudes Question Phrasing](#d-family-responsibilities-attitudes-question-phrasing)  

5. [Code Documentation](#5-code-documentation)  
	a. [Process Flow Diagram](#a-process-flow-diagram)  
	b. [Code Contents](#b-code-contents)  

6. [Extended Bibliography](#6-extended-bibliography)
<hr>

#### 0. Notes, Software, and Dependencies

1. All computational analysis was done using [Stata](https://www.stata.com/).    
2. All data visualization was done using [Microsoft Excel](https://www.microsoft.com/en-us/microsoft-365/excel).  
3. Exporting data to Excel from Stata was done using the Stata module [outreg2](https://ideas.repec.org/c/boc/bocode/s456416.html#:~:text=The%20functionality%20of%20outreg2%20is,outreg%2C%20by%20John%20Luke%20Gallup.), made by [Roy Wada](https://scholar.google.com/citations?user=I9hqGW0AAAAJ&hl=en).  
4. README.md file created using [Markdown Preview](https://github.com/facelessuser/MarkdownPreview), created and maintained by [Isaac Muse](https://github.com/facelessuser).
5. Multivariate regression estimated-R<sup>2</sup> values relying on multiple imputation were calculated using the Stata module [mibeta](https://www.stata.com/statalist/archive/2010-09/msg00630.html), made by [Yulia V. Marchenko](https://www.stata-journal.com/sjmatches.html?authorname=Yulia%20V.%20Marchenko).  
6. All [Gender Attitude Graphs](#2-gender-attitudes-over-time-by-political-preference) use variables that have been rescaled to range from 0 to 10.  
7. All multiple imputation calculations were administered using random-number seed 1234:
```
rseed(1234)
```   
8. All multiple imputation calculations of each dependent variable use 20 imputations:
```
add(20)
```   

<hr>

#### 1. Regression Tables  
**Please note:**  
- Standard errors are in parantheses following the coefficient.  
- p-values are calculated using a two-tailed test.  
- p-value indicators of all regression tables are as follows:  
```
  * p < 0.05
 ** p < 0.01
*** p < 0.001
```
- Regression table heads *Pre-Stall*, *Stall*, and *Post-Stall* inclusively refer to the following time periods:
```
 Pre-Stall: 1973-1993
     Stall: 1993-2004
Post-Stall: 2004-2018
```  

##### a. Multivariate Regression Tables - Interactive tables made available [here](./demonstratives/Multivariate_Regression_Tables.xlsx).  

###### i. Abortion Attitudes Multivariate Regression  
![Abortion_Reg](./assets/abortion_multivariate_results.png)  


###### ii. Sexual Behavior Attitudes Multivariate Regression  
![Sexatt_Reg](./assets/sexual_attitudes_multivariate_results.png)  


###### iii. Gender Roles Attitudes Multivariate Regression  
![Genrole_Reg](./assets/gender_roles_multivariate_results.png)  


###### iv. Family Responsibilities Attitudes Multivariate Regression  
![Famresp_Reg](./assets/family_responsibilities_multivariate_results.png)  


##### b. Ordinal Logistic Regression Tables - Interactive tables made available [here](./demonstratives/Ordinal_Logistic_Regression_Tables.xlsx).  

###### i. Abortion Attitudes Ordinal Logistic Regression  
![Abortion_oReg](./assets/abortion_ologit_results.png)  


###### ii. Sexual Behavior Attitudes Ordinal Logistic Regression  
![Sexatt_oReg](./assets/sexual_attitudes_ologit_results.png)  


###### iii. Gender Roles Attitudes Ordinal Logistic Regression  
![Genrole_oReg](./assets/gender_roles_ologit_results.png)  


###### iv. Family Responsibilities Attitudes Ordinal Logistic Regression  
![Famresp_oReg](./assets/family_responsibilities_ologit_results.png)  


##### c. Bivariate Regression Tables - Interactive tables made available [here](./demonstratives/Bivariate_Regression_Tables.xlsx).  


###### i. Abortion Attitudes Bivariate Regression  
![Abortion_biReg](./assets/abortion_bivariate_results.png)  


###### ii. Sexual Behavior Attitudes Bivariate Regression  
![Sexatt_biReg](./assets/sexual_attitudes_bivariate_results.png)  


###### iii. Gender Roles Attitudes Bivariate Regression  
![Genrole_biReg](./assets/gender_roles_bivariate_results.png)  


###### iv. Family Responsibilities Attitudes Bivariate Regression  
![Famresp_biReg](./assets/family_responsibilities_bivariate_results.png)  


<hr>

#### 2. Gender Attitudes Over Time by Political Preference  
Interactive data and charts made available [here](./demonstratives/Gender_Attitudes_by_Political_Preference.xlsx).


##### a. Mean Abortion Attitudes by Political Preference  
![Abortion_Att](./assets/mean_abortion_attitudes_political_pref.png)  


##### b. Standard Deviation of Abortion Attitudes by Political Preference  
![SD_Abortion_Att](./assets/sd_abortion_attitudes_political_pref.png)  


##### c. Mean Sexual Behavior by Political Preference  
![Sexatt_Att](./assets/mean_sexual_behavior_attitudes_political_pref.png)  


##### d. Standard Deviation of Sexual Behavior by Political Preference  
![SD_Sexatt_Att](./assets/sd_sexual_behavior_attitudes_political_pref.png)  


##### e. Mean Gender Role Attitudes by Political Preference  
![Genrole_Att](./assets/mean_gender_role_attitudes_political_pref.png)  


##### f. Standard Deviation of Gender Role Attitudes by Political Preference  
![SD_Genrole_Att](./assets/sd_gender_role_attitudes_political_pref.png)    


##### g. Mean Family Responsibilities Attitudes by Political Preference  
![Famresp_Att](./assets/mean_family_responsibilities_attitudes_political_pref.png)  


##### h. Standard Deviation of Family Responsibilities by Political Preference  
![SD_Famresp_Att](./assets/sd_family_responsibilities_attitudes_political_pref.png)  



<hr>

#### 3. Gender Attitudes Over Time by Race  
Interactive data and charts made available [here](./demonstratives/Gender_Attitudes_by_Race.xlsx).  


##### a. Mean Abortion Attitudes by Race  
![Abortion_Att_R](./assets/mean_abortion_attitudes_race.png)  


##### b. Standard Deviation of Abortion Attitudes by Race  
![SD_Abortion_Att_R](./assets/sd_abortion_attitudes_race.png)  


##### c. Mean Sexual Behavior by Race  
![Sexatt_Att_R](./assets/mean_sexual_behavior_attitudes_race.png)  


##### d. Standard Deviation of Sexual Behavior by Race  
![SD_Sexatt_Att_R](./assets/sd_sexual_behavior_attitudes_race.png)  


##### e. Mean Gender Role Attitudes by Race  
![Genrole_Att_R](./assets/mean_gender_role_attitudes_race.png)  


##### f. Standard Deviation of Gender Role Attitudes by Race  
![SD_Genrole_Att_R](./assets/sd_gender_role_attitudes_race.png)    


##### g. Mean Family Responsibilities Attitudes by Race  
![Famresp_Att_R](./assets/mean_family_responsibilities_attitudes_race.png)  


##### h. Standard Deviation of Family Responsibilities by Race  
![SD_Famresp_Att_R](./assets/sd_family_responsibilities_attitudes_race.png)  

<hr>

#### 4. Dependent Variable Question Phrasing

##### a. Abortion Attitudes Question Phrasing  
1. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if the family has a very low income and cannot afford any more children? (**GSS Variable:** [abpoor](https://gssdataexplorer.norc.org/variables/604/vshow))  

2. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if the woman's own health is seriously endangered by the pregnancy? (**GSS Variable:** [abhlth](https://gssdataexplorer.norc.org/variables/603/vshow))  

3. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if she is married and does not want any more children? (**GSS Variable:** [abnomore](https://gssdataexplorer.norc.org/variables/602/vshow))  

4. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if there is a strong chance of serious defect in the baby? (**GSS Variable:** [abdefect](https://gssdataexplorer.norc.org/variables/601/vshow))  

5. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if she became pregnant as a result of rape? (**GSS Variable:** [abrape](https://gssdataexplorer.norc.org/variables/605/vshow))  

6. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if she is not married and does not want to marry the man? (**GSS Variable:** [absingle](https://gssdataexplorer.norc.org/variables/606/vshow))  

7. Please tell me whether or not you think it should be possible for a pregnant woman to obtain a legal abortion if the woman wants it for any reason? (**GSS Variable:** [abany](https://gssdataexplorer.norc.org/variables/607/vshow))  

##### b. Sexual Behavior Attitudes Question Phrasing

1. Would you be for or against sex education in the public schools? (**GSS Variable:** [sexeduc](https://gssdataexplorer.norc.org/variables/626/vshow))  

2. There's been a lot of discussion about the way morals and attitudes about sex are changing in this country. If a man and woman have sex relations before marriage, do you think it is always wrong, almost always wrong, wrong only sometimes, or not wrong at all? (**GSS Variable:** [premarsx](https://gssdataexplorer.norc.org/variables/631/vshow))  

3. Questions associated with this variable: There's been a lot of discussion about the way morals and attitudes about sex are changing in this country. If a man and woman have sex relations before marriage, do you think it is always wrong, almost always wrong, wrong only sometimes, or not wrong at all? A. What if they are in their early teens, say 14 to 16 years old? In that case, do you think sex relations before marriage are always wrong, almost always wrong, wrong only sometimes, or not wrong at all? (**GSS Variable:** [teensex](https://gssdataexplorer.norc.org/variables/632/vshow))  

4. What about sexual relations between two adults of the same sex--do you think it is always wrong, almost always wrong, wrong only sometimes, or not wrong at all? (**GSS Variable:** [homosex](https://gssdataexplorer.norc.org/variables/634/vshow))   

5. What is your opinion about a married person having sexual relations with someone other than the marriage partner--is it always wrong, almost always wrong, wrong only sometimes, or not wrong at all? (**GSS Variable:** [xmarsex](https://gssdataexplorer.norc.org/variables/633/vshow))  

##### c. Gender Roles Attitudes Question Phrasing  
1. Tell me if you agree or disagree with this statement: Most men are better suited emotionally for politics than are most women. (**GSS Variable:** [fepol](https://gssdataexplorer.norc.org/variables/591/vshow))  

##### d. Family Responsibilities Attitudes Question Phrasing  
Now I'm going to read several more statements. As I read each one, please tell me whether you strongly agree, agree, disagree, or strongly disagree with it. For example, here is the statement:  

1. A working mother can establish just as warm and secure a relationship with her children as a mother who does not work. (**GSS Variable:** [fechld](https://gssdataexplorer.norc.org/variables/703/vshow))  

2. A preschool child is likely to suffer if his or her mother works. (**GSS Variable:** [fepresch](https://gssdataexplorer.norc.org/variables/705/vshow))  

3. It is much better for everyone involved if the man is the achiever outside the home and the woman takes care of the home and family. (**GSS Variable:** [fefam](https://gssdataexplorer.norc.org/variables/706/vshow))  

<hr>

#### 5. Code Documentation  

##### a. Process flow diagram  
To aid in replicating the data shared in this study and repository, a process flow diagram beginning with GSS Data and ending with regression tables/attitude summarizations is provided below:   

![Process_Flow](./assets/process_flow_diagram.png)  

##### b. Code Contents

1. Selected GSS variables for this study are found here: [RAW_GSS_SELECTED_VARIABLES.dta](./do/RAW_GSS_DATA_SELECTED_VARIABLES.dta)  

2. Code to filter the [selected GSS variables](./do/RAW_GSS_DATA_SELECTED_VARIABLES.dta) and generate attitude scales are found here: [1_variable_filter.do](./do/1_variable_filter.do)  

3. [The variable filter](./do/1_variable_filter.do) outputs filtered/processed variables here: [ALL_FINAL_VARIABLES_PROCESSED.dta](./do/ALL_FINAL_VARIABLES_PROCESSED.dta)  

4. To impute missing data in the [processed dataset](./do/ALL_FINAL_VARIABLES_PROCESSED.dta), execute the multiple imputation code, found here: [2_multiple_imputation_data_creation.do](./do/2_multiple_imputation_data_creation.do)  

5. [The imputation code](./do/2_multiple_imputation_data_creation.do) outputs an imputed dataset for each independent variable:
	- [abscale_multiple_imputation.dta](./do/mi_results_and_regressions/abscale_multiple_imputation.dta)  
	- [sexatt_multiple_imputation.dta](./do/mi_results_and_regressions/sexatt_multiple_imputation.dta)  
	- [genrole_multiple_imputation.dta](./do/mi_results_and_regressions/genrole_multiple_imputation.dta)  
	- [famresp_multiple_imputation.dta](./do/mi_results_and_regressions/famresp_multiple_imputation.dta)  

6. Regression models are computed using the [imputed datasets](./do/mi_results_and_regressions). The following regression computations available are:  
	- [Bivariate Regression](./do/mi_results_and_regressions/bivariate_regression.do)  
	- [Multivariate Regression](./do/mi_results_and_regressions/multivariate_regression.do)  
	- [Ordinal Logistic Regression](./do/mi_results_and_regressions/ologit_regression.do)  

7. Summary data is generated using the [non-imputed dataset](./do/ALL_FINAL_VARIABLES_PROCESSED.dta), code found here: [3_generate_attitude_summarizations.do](./do/3_generate_attitude_summarizations.do)  
8. ```.do``` files output ```.log``` files in the the same directory in which the ```.do``` file is executed. 

<hr>

#### 6. Extended Bibliography  

To view the extended bibliography for this paper, please click [here](https://anon-subsoci.github.io/Anonymous-Gender-Attitudes-Appendix/.).  
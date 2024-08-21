# CAnD3-RRWM-Data-Activity
  Research Replicability and Workflow Management - Exercise 1

## Objective:
  Explore the relationship between family composition and social context variables and self-rated health. 

## Data: 
  The Canadian "General Social Survey - Family" from 2017 (GSS) is used for the following analysis. 

## Filtering and Renaming:
  Observations that were uninformative were removed. The filtering process follows this criteria:

   Self Rated Health (SRH_110):
    ●	Only responses ranking their health from 'Excellent (1)' to 'Poor (5)' were included.
    ●	Responses outside this range or those which were not categorized between 1 to 5 were excluded.

   Income of Respondent (TTLINCG2):
    ●	Responses indicating income ranges from <$25,000 (1) to $125,000 or more (5) were retained.
    ●	Responses outside these specific categories were omitted.

   Household Size of Respondent (HSDSIZEC):
    ●	Retained households sizes from 'One person household (1)' to 'Six or more person household (6)'.
    ●	Any other factors outside this range were discarded.

   Population Center Indicator (LUC_RST):
    ●	Three types of population centers were included: 'Larger urban population centers (1)', 'Rural areas and small population centers (2)', and 'Prince Edward Island (3)'.
    ●	Responses outside these categories were excluded.

   Birth or Adoption (GU_110):
    ●	Distinguished between respondents who answered 'Yes (both birth parents) (1)', 'Yes (both adoptive parents) (2)', and 'No (3)'.
    ●	Other responses were excluded.

   Age When Parents Divorced (APARDIVC):
    ●	Respondents who mentioned their age when their parents divorced, but capped at age 35 and older (from 0-35 years). The only other categories considered were 'Valid Skip (96)' and 'Don't Know (97)'.

   Dwelling - Owned or Rented (ODR_10):
    ●	Only responses indicating 'Owned by (1)' and 'Rented (2)' were kept.

   Average Hours Worked per Week (UHW_16GR):
    ●	Categories from '0 hours (1)' to '50.1 hours and more (5)' were included, along with 'Valid Skip (6)'.

   Place of Birth of Respondent (BRTHMACR):
    ●	Responses indicating places like the Americas (1), Europe (2), Africa (3), Asia (4), Oceania, and others (5) were retained.


  ## Renaming:

   For the ease of reference and to ensure clarity during the analysis, several variables were renamed. Here are the old variable names and their corresponding new names:

   ●	SRH_110 became srh
   ●	TTLINCG2 became totinc
   ●	HSDSIZEC became hhsize
   ●	LUC_RST became rururb
   ●	GU_110 became adopt
   ●	UHW_16GR became avghw
   ●	APARDIVC became divorce
   ●	ODR_10 became hmown
   ●	BRTHMACR became bplace


  ## Table of Summary/Descriptive Statistics:
   Descriptive statistics, including mean and standard deviation, were computed for all key variables.


  ## Recoding: 
   The binary recoding process involved reclassifying variables like 'adopt' and 'hmown'. For instance, the variable 'adopt' was recoded so that 'No' became '1' and 'Yes' (either adoptive or birth) became '0'. This    
   sets a reference category against which other categories can be compared. 

   Nominal recoding process involves converting the 'bplace' and 'rururb' variables into factors. 


  ## OLS Regression:
   ●	A linear regression (OLS) was conducted to predict self-rated health based on various predictors.
   ●	Regression results (Table 2) were displayed with coefficients, standard errors, t-values, and p-values for each predictor variable.

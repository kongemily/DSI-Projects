# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

### Emily Kong, DSI-14-Singapore


### Problem Statement 

This report sets out to identify potential relationships between 2017-2018 SAT and ACT participation rates and scores, as well as State Debt and State Income Statistics and further analyse the data to identify opportunities for increasing SAT participation rates.

---

### Executive Summary 

The Common Core State Standards Initiatives seeks to establish consistent educational standards across the states as well as ensure that students graduating from high school are prepared to enter credit-bearing courses. Forty-two states, District of Columbia have chosen to adopt these Standards although no exact requirements for curriculum, schools and districts are specified. Both SAT and ACT test accomplish many of the goals aligned with the Common Core Standards.

This project sets out to examine the data covering participation rates and scores for both ACT and SAT for 2017 and 2018 at state levels. This allowed for exploration of any relationships between the participation rates for the 2 tests and the respective scores. A further analysis of correlations was performed between the participation rates, state income and state debt. 

The observations from the data was consistent with research articles stating more US states mandated ACT as a state administered test with 17 states achieving 100% participation rates in 2017 compared to only 4 States for SAT. The negative correlation between the participation rates for both tests also indicated that only one of the two tests were usually taken and States with low participation scores had higher average scores for the tests. 

From the data obtained, one of the key observations noted was positive correlation between SAT participation rates in 2017/2018 with median household income, median family income and per capita income, whereas the same correlation did not exist for ACT participation rates. Therefore, further analysis was performed for participation rates against state debt levels to confirm if this holds through. However, it was found that there was positive correlation between SAT participation rates with state debt and negative correlation between ACT participation rates with state debt. However, it is not conclusive if these debts are also in relation to college loans or funds budgeted by respective states for education. As mentioned on [Collgevine's blog](https://blog.collegevine.com/the-most-helpful-khan-academy-sat-resources/), test prep for SAT was previously an exclusive privilege, limited by its high costs. This is in line with the positive correlation of SAT participation rates and state income statistics. This was also mentioned by [Prep Scholar](https://blog.prepscholar.com/which-states-require-the-sat) that College Board had introduced a program to increase access of SAT to low-income students, but it was still considered to test aptitude rather than knowledge. However, with the introduction of a redesigned SAT in 2016 to align with the Common Core standards, this  could have partially contributed to the State's decision to shift of ACT to SAT as the standardised test for Illnois and Colorado in 2017. 

### Conclusions and Recommendations

Based on the research articles, the participation rates for both tests were partially a result of state policy with 29 states requiring either SAT or ACT. However, both tests are accepted by colleges and univerisities as part of the admission criterias. 

Consider the case of Colorado where the state education board made the decision to switch from ACT to SAT as the standardised test for the State which resulted in the sharp increase in SAT's participation rate in 2018 accompanied by a corresponding sharp fall in ACT participation rate.  [Colorado Kids](https://www.coloradokids.org/wp-content/uploads/2016/01/ACTvsSAT_FINAL.pdf) had published an article of the decision by Colorado to shift from ACT to SAT and the College Board should take reference from this success and consequently, increase efforts in the following aspects in order to increase its participation rates. 

- Offering free SAT preparation course online 
- Targeting high-achieving, low-income students and provide them with the same opportunities 
- Continue efforts to align SAT tests to Common Core standards

Further reasearch into correlation between college debt and participation rates will be of particular interest and may provide valuable insight with the increasing focus of mounting college debts. However, no comprehensive statistics was found for all the states at this stage.

#### Datasets

For this project, first four datasets were provided and 2 more from the internet:

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018_updated.csv)
- [State Income 2010-2014](./data/stateincome.csv)
- [State Debt 2020](./data/statedebt.csv)

#### Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|final|U.S. States|
|sat18_participation|float|final|Participation rates for SAT in 2018 across the States|
|sat18_read_and_write|float|final|Average Score for SAT Read and Write in 2018|
|sat18_math|float|final|Average Score for SAT Math in 2018|
|total_sat18|float|final|Average Total Score for SAT in 2018|
|act18_participation|float|final|Participation rates for ACT in 2018 across the States|
|act18_composite|float|final|Average Composite Score for ACT in 2018|
|act18_english|float|final|Average Score for ACT English in 2018|
|act18_math|float|final|Average Score for ACT Math in 2018|
|act18_reading|float|final|Average Score for ACT Reading in 2018|
|act18_science|float|final|Average Score for ACT Science in 2018|
|sat17_participation|float|final|Participation rates for SAT in 2017 across the States|
|sat17_read_and_write|float|final|Average Score for SAT Read and Write in 2017|
|sat17_math|float|final|Average Score for SAT Math in 2017|
|act17_participation|float|final|Participation rates for ACT in 2017 across the States|
|act17_composite|float|final|Average Composite Score for ACT in 2017|
|act17_english|float|final|Average Score for ACT English in 2017|
|act17_math|float|final|Average Score for ACT Math in 2017|
|act17_reading|float|final|Average Score for ACT Reading in 2017|
|act17_science|float|final|Average Score for ACT Science in 2017|
|state|object|stateincome|U.S. States|
|per_capita_income|float|stateincome|Per capita income for each State from 2010-2014|
|median_household_income|float|stateincome|Median household income for each State from 2010-2014|
|population|float|stateincome|Population for each State from 2010-2014|
|number_of_households|float|stateincome|Number of households for each State from 2010-2014|
|number_of_families|float|stateincome|Number of families for each State from 2010-2014|
|state|object|statedebt|U.S. States|
|debt|int|statedebt|Total debt per state for 2020|
|per_capita|int|statedebt|Per capita debt per State for 2020|
|population|int|statedebt|Population for each State for 2020|





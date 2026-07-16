## Assessing Healthcare Access Risk by Predicting Hospital Closures
Training a machine learning model on various public health data to predict and assess the probability that a county experiences a hospital closure within the next few years.

### Introduction
Hospital closures are becoming more common in the United States. While many communities are facing change or decline in the face of rapidly shifting economic and demographic trends, for-profit hospital systems are faced with a choice: continue serving a community in spite of operational underperformance, make the healthcare operations more profitable, or cease operations in a geography entirely. 

Another notable trend is consolidation of businesses in healthcare. In addition to hospitals, it is also impacting specific fields of medicine like dental and veterinary practices. While the corporate consolidation of healthcare (or less competition in a geography) may lead to beneficial impacts at scale, it often does not serve the community who may face greater costs, poorer service, and greater risk when large-scale changes (e.g. fewer in-network insurers) are not met with competitive alternatives in that geography. 

Hospital closures - especially when they entirely remove healthcare access from a community - often lead to severe consequences for those affected communities, leading to further decline and decay of the population and health over time that is extremely hard to recover from. 

This analysis aims to understand hospital closures nationwide through public health data (namely, the AHRF's hospital counts) and then supplement the core dataset with additional county-level data sources to provide an in-depth statistical analysis and forecast that can help identify at-risk the communities and populations that are likely to face further decline or divestment in the future.


### Overview
This project intends to address:
- Various sources of public health data & why they matter 
- Data engineering work to combine the various data
- Data science techniques to analyze the factors most correlated with (or that most often precede) hospital closures
- Machine learning techniques to train a model on historical data and then forecast hospital closures into the future
- Visualizations of various data elements at the county level to see and interact with data and trends
- Conclusive explanations of findings and how this new information can be further utilized

### Evaluating Sources of Public Health Data 

The following factors are generally considered to play a role in most hospital closures:
- Population decline (often leading to fewer patients and workforce shortages)
- Higher financial stress (from a mix of factors including lower insurance coverage, lower utilization of services, and competition from larger hospital systems)
- Increasing poverty and chronic disease burden along with decreased economic growth
- Geographic isolation (rurality)

- and likely more. The next step is to identify publicly accessible data that can provide context in these areas and beyond.

#### Valuable public health datasets available at the county-level that can provide context in these areas:

#### Area Health Resources Files (AHRF) / National Center for Health Workforce Analysis

Provides the following at the county-level:
- Physician counts
- Nurse counts
- Hospital counts
- Other health workforce measures

Why it matters: This data is critical to understand the number of hospitals and workforce shortages over time as they precede hospital closures.


#### U.S. Census / American Community Survey (ACS)

Provides the following at the county-level:

- Population growth/decline
- Median income
- Poverty
- Age distribution
- Education
- Disability rates

Why it matters: Population decline is one of the strongest structural threats to hospitals. Aging and shrinking communities often lose hospital inpatient volume when the population gets smaller. Hospitals need to operate at scale to be viable and profitable. Additionally, other factors such as poverty, education, and disability rates can also be highly indicative of the overall health and long-term trends of a given population. 

#### CMS Geographic Data / Centers for Medicare and Medicaid

Provides the following at the county-level:

- Medicare enrollment
- Medicare spending
- Beneficiary demographics

Why it matters: Hospitals heavily depend on CMS (Medicare & Medicaid) reimbursement, as those covered otherwise many not be able to afford or recieve care. At the same time, populations with high Medicare & Medicaid enrollment can create financial pressures for hospitals, as there tends to be lower profit margins for care provided to these beneficiaries. Enrollment rates and other demographic factors (especially in conjunction with other data such as poverty rates provided by the U.S. Census) can be highly indicative of population trends that impact hospital performance. 


#### Other important supplementary data sources:

#### County Health Rankings & Roadmaps

Aggregates the following at the county-level:
- Health outcomes
- Health behaviors
- Clinical care access
- Social determinants

Why it matters: Many researchers use this source as a summary measure of county health.


#### CDC PLACES / CDC 

Provides county-level estimates for:
- Diabetes
- Obesity
- Smoking
- Physical inactivity
- Hypertension
- Mental health indicators

Why it matters: 
- Poor population health affects payer mix, utilization patterns, and healthcare costs.
- Counties with high chronic disease burdens often overlap with economically distressed regions.


#### Bureau of Labor Statistics (BLS)

Provides the following at the county-level:
- Unemployment rate 
- Underemployment rate
- Labor force participation rate

Why it matters: Economic distress predicts healthcare system instability. If unemployment in a population is going up, or if underemployment is rising, or the percentage of the population actually participating in the workforce is declining, these can all correlate with declining healthcare coverage or worsening quality of coverage (e.g. if a person previously recieved benefits through their job, then they begin to recieve benefits under Medicare/Medicaid, that can lead to less profit margin for a hospital or provider treating that person).


#### Rural-Urban Continuum Codes / United States Department of Agriculture

This data measures the following:
- Rurality
- Distance from metropolitan areas

Why it matters: Rural hospitals close at much higher rates. 


#### Social Vulnerability Index (SVI) / CDC

Includes:
- Poverty
- Transportation access
- Housing instability
- Language barriers

Why it matters: Captures broader community vulnerability.

#### Data elements grouped into categories:

Healthcare Access:
- Number of hospitals (AHRF)
- Number of nurses and physicians (AHRF)
- Rurality score, travel time to nearest hospital, nearby hospital capacity (RUCC)

Demographics:
- Population growth, population density (Census)
- Elderly population % 

Economics:
- Median income (US Census)
- Poverty rate (US Census)
- Unemployment, underemployment, LFPR (BLS)

Population Health:
- Diabetes (CDC)
- Obesity (CDC)
- Smoking (CDC)

#### Additional supplementary datasets to explore and include
- County level opiod and infant mortality (may not be needed but there is data available)
- Climate and weather data (especially relevant in the context of climate change risk)

### Simple analysis on hospital shortages
This section will address the AHRF data specifically as it is integral to understand hospital numbers at the county-level over time. 

As a bonus, GIS mapping of hospital numbers over time nationwide (at the county-level using FIPS codes) would be beneficial.

### Combining various datasets together
This section will walk through the data engineering steps to create a singlular dataset that can be utilized for machine learning and forecasting.


### Applying statistical and machine learning techniques to the unified dataset
This section will seek to understand what factors are most correlated with declining hospital numbers as well as train a model to predict hospital closures into the future. It may also include the creation of a "Hospital Vulnerability Index" or "Healthcare Access Risk Index" to indicate which counties are most at-risk of decline and/or divestment.


### In-depth analysis on the forecasting of hospital closures
This section will explain the outcome of the applied statistical and machine learning techniques. As a bonus, mapping counties nationwide using their FIPS codes to visualize the Hospital Vulnerability Index would be beneficial.


### Additional Analysis, Insights, Visualization (TBD)
[Work in Progress (WIP)]


### Conclusion 
[Work in Progress (WIP)]


### Resources
#### On Hospital Closures

National Rural Health Association - Advocacy 
- https://www.ruralhealth.us/advocacy/advocacy-priority-areas/hospitals-health-systems

UNC Center Health Services Research - Interactive Dashboard 
- https://www.shepscenter.unc.edu/programs-projects/rural-health/rural-hospital-closures/

Chartis State of Rural Health 2025 - Research 
- https://www.chartis.com/insights/2025-rural-health-state-state 

PA Senate Hearing on Healthcare Accessibility and Hospital Closure Impacts 
- https://pasenate.com/senate-democratic-caucus-policy-chair-nick-miller-hosts-hearing-examining-healthcare-accessibility-and-hospital-closure-impacts/ 


#### On Data Sources

Area Health Resource Files / HRSA Data Warehouse
- https://data.hrsa.gov/topics/health-workforce/nchwa/ahrf

U.S Census Data
- https://www.census.gov/programs-surveys/acs/data.html

CMS Data
- https://data.cms.gov/summary-statistics-on-use-and-payments/medicare-geographic-comparisons/medicare-geographic-variation-by-national-state-county

CDC Data
- https://www.cdc.gov/places/index.html 

BLS Data
- https://www.bls.gov/

## Assessing Healthcare Access Risk by Predicting Hospital Closures
Training a machine learning model on various public health data to predict and assess the probability that a county experiences a hospital closure within the next few years.

### Introduction


### Overview


### Evaluating Sources of Public Health Data 

Hospital closures are commonly associated with the following:
- Population decline (often leading to fewer patients and workforce shortages)
- Higher financial stress (from a mix of factors including lower insurance coverage, lower utilization of services, and competition from larger hospital systems)
- Increasing poverty and chronic disease burden along with decreased economic growth
- Geographic isolation (rurality)

and likely more. 

#### Valuable public health datasets available at the county-level that can provide context in these areas:

- Area Health Resources Files (AHRF)
Provides:
Physician counts
Nurse counts
Hospital counts
Health workforce measures
Why it matters: Critical to understand number of hospitals and workforce shortages


U.S. Census / American Community Survey (ACS)
Provides:
Population growth/decline
Median income
Poverty
Age distribution
Education
Disability rates

Why it matters:
Population decline is one of the strongest structural threats to hospitals.
Aging and shrinking communities often lose inpatient volume.

CMS Geographic Data
County-level:
Medicare enrollment
Medicare spending
Beneficiary demographics

Why it matters:
Hospitals heavily depend on Medicare reimbursement.
High Medicare populations can create financial pressures.


#### Important supplementary data sources:

County Health Rankings & Roadmaps

Aggregates:
Health outcomes
Health behaviors
Clinical care access
Social determinants

Why it matters:
Many researchers use it as a summary measure of county health.


CDC PLACES
Provides county-level estimates for:
Diabetes
Obesity
Smoking
Physical inactivity
Hypertension
Mental health indicators

Why it matters:
Poor population health affects payer mix, utilization patterns, and healthcare costs.
Counties with high chronic disease burdens often overlap with economically distressed regions.


Bureau of Labor Statistics (BLS)
County-level:
Unemployment
Labor force participation
Why it matters:
Economic distress predicts healthcare system instability.


Rural-Urban Continuum Codes
From the United States Department of Agriculture

Measures:
Rurality
Distance from metropolitan areas

Why it matters:
Rural hospitals close at much higher rates.

Social Vulnerability Index (SVI). From the CDC.

Includes:
Poverty
Transportation access
Housing instability
Language barriers

Why it matters:
Captures broader community vulnerability.
Opioid and Mortality Data
County-level:
Drug deaths
Premature mortality

Why it matters:
Signals broader socioeconomic distress.


Data elements grouped into categories:

Healthcare Access:
- Number of hospitals (AHRF)
- Number of nurses and physicians (AHRF)
- Rurality score, travel time to nearest hospital, nearby hospital capacity

Demographics:
- Population growth, population density
Elderly population %

Economics:
- Median income
- Poverty rate
- Unemployment, underemployment

Population Health:
- Diabetes
- Obesity
- Smoking






### Resources

National Rural Health Association - Advocacy 
https://www.ruralhealth.us/advocacy/advocacy-priority-areas/hospitals-health-systems

UNC Center Health Services Research - Interactive Dashboard 
https://www.shepscenter.unc.edu/programs-projects/rural-health/rural-hospital-closures/

Chartis State of Rural Health 2025 - Research 
 https://www.chartis.com/insights/2025-rural-health-state-state 

PA Senate Hearing on Healthcare Accessibility and Hospital Closure Impacts https://pasenate.com/senate-democratic-caucus-policy-chair-nick-miller-hosts-hearing-examining-healthcare-accessibility-and-hospital-closure-impacts/ 



<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-MML-AM_CHTML" type="application/javascript"></script>

Problem Description
============

<!-- TOC START min:1 max:3 link:true update:true -->
  - [About the data](#about-the-data)
  - [Target Variable](#target-variable)
    - [Submission Format](#submission-format)
    - [Performance Metric](#performance-metric)
  - [Features](#features)
    - [Categories](#categories)
    - [Example Row](#example-row)
<!-- TOC END -->

<a id="about-the-data"></a>

## About the data

Your goal is to predict a student's earnings a set number of years after they have enrolled in United States institutions of higher education. The data is compiled from a wide range of sources and [made publicly available by the United States Department of education](https://collegescorecard.ed.gov/).

<a id="target-variable"></a>

## Target Variable

We're trying to predict the variable `income`, which represents earnings **in thousands of US dollars** a set interval
from when the student first enrolled.

<a id="submission-format"></a>

### Submission Format

The format for the submission file is two columns with the `row_id` and the `income`. The data type of `income` is a float, **so make sure there is a decimal point in your submission**. For example `0.0` is a valid float. `0` is _not_.

<div class="well">

For example, if you predicted...

| row_id | income |
|--------|--------|
|      2 |    0.0 |
|      8 |    0.0 |
|      9 |    0.0 |
|     10 |    0.0 |
|     11 |    0.0 |

The first few lines of the `.csv` file that you submit would look like:

    row_id,income
    2,0.0
    8,0.0
    9,0.0
    10,0.0
    11,0.0

<a id="performance-metric"></a>

### Performance Metric

We're predicting a numeric quantity, so this is a regression problem. To measure regression, we'll use a metric called Root-mean-squared error. It is an error metric, so lower value is better (as opposed to an accuracy metric, where a higher value is better).

$$RMSE = \sqrt{\frac{1}{N}\sum_{n=1}^{N} (\hat{y}_n - y_n)^2  }$$

Where $\hat{y}_n$ is the predicted earnings and $y_n$ is the actual earnings. The best possible score is 0, but the worst possible score can be infinite.


<a id="features"></a>

## Features

There are 297 variables in this dataset. Each row in the dataset represents a United States institution of higher education in a specific year. The dataset we are working with covers four particular years, denoted `year_a`, `year_f`, `year_w`, and `year_z` in our dataset. An institution may have a row for all, some, or just for one of the years. We don't provide a unique identifier for an individual institution, just a `row_id` for each row.

The variables in the dataset have names that of the form `category__variable`, where `category` is the high level category of the variable (e.g. `academics` or `students`). `variable` is what the specific column contains.

<a id="categories"></a>

### Categories


 - **`academics`**

    - `program_assoc_agriculture`: Associate degree in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_assoc_architecture`: Associate degree in Architecture And Related Services.
    - `program_assoc_biological`: Associate degree in Biological And Biomedical Sciences.
    - `program_assoc_business_marketing`: Associate degree in Business, Management, Marketing, And Related Support Services.
    - `program_assoc_communication`: Associate degree in Communication, Journalism, And Related Programs.
    - `program_assoc_communications_technology`: Associate degree in Communications Technologies/Technicians And Support Services.
    - `program_assoc_computer`: Associate degree in Computer And Information Sciences And Support Services.
    - `program_assoc_construction`: Associate degree in Construction Trades.
    - `program_assoc_education`: Associate degree in Education.
    - `program_assoc_engineering`: Associate degree in Engineering.
    - `program_assoc_engineering_technology`: Associate degree in Engineering Technologies And Engineering-Related Fields.
    - `program_assoc_english`: Associate degree in English Language And Literature/Letters.
    - `program_assoc_ethnic_cultural_gender`: Associate degree in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_assoc_family_consumer_science`: Associate degree in Family And Consumer Sciences/Human Sciences.
    - `program_assoc_health`: Associate degree in Health Professions And Related Programs.
    - `program_assoc_history`: Associate degree in History.
    - `program_assoc_humanities`: Associate degree in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_assoc_language`: Associate degree in Foreign Languages, Literatures, And Linguistics.
    - `program_assoc_legal`: Associate degree in Legal Professions And Studies.
    - `program_assoc_library`: Associate degree in Library Science.
    - `program_assoc_mathematics`: Associate degree in Mathematics And Statistics.
    - `program_assoc_mechanic_repair_technology`: Associate degree in Mechanic And Repair Technologies/Technicians.
    - `program_assoc_military`: Associate degree in Military Technologies And Applied Sciences.
    - `program_assoc_multidiscipline`: Associate degree in Multi/Interdisciplinary Studies.
    - `program_assoc_parks_recreation_fitness`: Associate degree in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_assoc_personal_culinary`: Associate degree in Personal And Culinary Services.
    - `program_assoc_philosophy_religious`: Associate degree in Philosophy And Religious Studies.
    - `program_assoc_physical_science`: Associate degree in Physical Sciences.
    - `program_assoc_precision_production`: Associate degree in Precision Production.
    - `program_assoc_psychology`: Associate degree in Psychology.
    - `program_assoc_public_administration_social_service`: Associate degree in Public Administration And Social Service Professions.
    - `program_assoc_resources`: Associate degree in Natural Resources And Conservation.
    - `program_assoc_science_technology`: Associate degree in Science Technologies/Technicians.
    - `program_assoc_security_law_enforcement`: Associate degree in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_assoc_social_science`: Associate degree in Social Sciences.
    - `program_assoc_theology_religious_vocation`: Associate degree in Theology And Religious Vocations.
    - `program_assoc_transportation`: Associate degree in Transportation And Materials Moving.
    - `program_assoc_visual_performing`: Associate degree in Visual And Performing Arts.
    - `program_bachelors_agriculture`: Bachelor's degree in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_bachelors_architecture`: Bachelor's degree in Architecture And Related Services.
    - `program_bachelors_biological`: Bachelor's degree in Biological And Biomedical Sciences.
    - `program_bachelors_business_marketing`: Bachelor's degree in Business, Management, Marketing, And Related Support Services.
    - `program_bachelors_communication`: Bachelor's degree in Communication, Journalism, And Related Programs.
    - `program_bachelors_communications_technology`: Bachelor's degree in Communications Technologies/Technicians And Support Services.
    - `program_bachelors_computer`: Bachelor's degree in Computer And Information Sciences And Support Services.
    - `program_bachelors_construction`: Bachelor's degree in Construction Trades.
    - `program_bachelors_education`: Bachelor's degree in Education.
    - `program_bachelors_engineering`: Bachelor's degree in Engineering.
    - `program_bachelors_engineering_technology`: Bachelor's degree in Engineering Technologies And Engineering-Related Fields.
    - `program_bachelors_english`: Bachelor's degree in English Language And Literature/Letters.
    - `program_bachelors_ethnic_cultural_gender`: Bachelor's degree in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_bachelors_family_consumer_science`: Bachelor's degree in Family And Consumer Sciences/Human Sciences.
    - `program_bachelors_health`: Bachelor's degree in Health Professions And Related Programs.
    - `program_bachelors_history`: Bachelor's degree in History.
    - `program_bachelors_humanities`: Bachelor's degree in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_bachelors_language`: Bachelor's degree in Foreign Languages, Literatures, And Linguistics.
    - `program_bachelors_legal`: Bachelor's degree in Legal Professions And Studies.
    - `program_bachelors_library`: Bachelor's degree in Library Science.
    - `program_bachelors_mathematics`: Bachelor's degree in Mathematics And Statistics.
    - `program_bachelors_mechanic_repair_technology`: Bachelor's degree in Mechanic And Repair Technologies/Technicians.
    - `program_bachelors_military`: Bachelor's degree in Military Technologies And Applied Sciences.
    - `program_bachelors_multidiscipline`: Bachelor's degree in Multi/Interdisciplinary Studies.
    - `program_bachelors_parks_recreation_fitness`: Bachelor's degree in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_bachelors_personal_culinary`: Bachelor's degree in Personal And Culinary Services.
    - `program_bachelors_philosophy_religious`: Bachelor's degree in Philosophy And Religious Studies.
    - `program_bachelors_physical_science`: Bachelor's degree in Physical Sciences.
    - `program_bachelors_precision_production`: Bachelor's degree in Precision Production.
    - `program_bachelors_psychology`: Bachelor's degree in Psychology.
    - `program_bachelors_public_administration_social_service`: Bachelor's degree in Public Administration And Social Service Professions.
    - `program_bachelors_resources`: Bachelor's degree in Natural Resources And Conservation.
    - `program_bachelors_science_technology`: Bachelor's degree in Science Technologies/Technicians.
    - `program_bachelors_security_law_enforcement`: Bachelor's degree in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_bachelors_social_science`: Bachelor's degree in Social Sciences.
    - `program_bachelors_theology_religious_vocation`: Bachelor's degree in Theology And Religious Vocations.
    - `program_bachelors_transportation`: Bachelor's degree in Transportation And Materials Moving.
    - `program_bachelors_visual_performing`: Bachelor's degree in Visual And Performing Arts.
    - `program_certificate_lt_1_yr_agriculture`: Certificate of less than one academic year in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_certificate_lt_1_yr_architecture`: Certificate of less than one academic year in Architecture And Related Services.
    - `program_certificate_lt_1_yr_biological`: Certificate of less than one academic year in Biological And Biomedical Sciences.
    - `program_certificate_lt_1_yr_business_marketing`: Certificate of less than one academic year in Business, Management, Marketing, And Related Support Services.
    - `program_certificate_lt_1_yr_communication`: Certificate of less than one academic year in Communication, Journalism, And Related Programs.
    - `program_certificate_lt_1_yr_communications_technology`: Certificate of less than one academic year in Communications Technologies/Technicians And Support Services.
    - `program_certificate_lt_1_yr_computer`: Certificate of less than one academic year in Computer And Information Sciences And Support Services.
    - `program_certificate_lt_1_yr_construction`: Certificate of less than one academic year in Construction Trades.
    - `program_certificate_lt_1_yr_education`: Certificate of less than one academic year in Education.
    - `program_certificate_lt_1_yr_engineering`: Certificate of less than one academic year in Engineering.
    - `program_certificate_lt_1_yr_engineering_technology`: Certificate of less than one academic year in Engineering Technologies And Engineering-Related Fields.
    - `program_certificate_lt_1_yr_english`: Certificate of less than one academic year in English Language And Literature/Letters.
    - `program_certificate_lt_1_yr_ethnic_cultural_gender`: Certificate of less than one academic year in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_certificate_lt_1_yr_family_consumer_science`: Certificate of less than one academic year in Family And Consumer Sciences/Human Sciences.
    - `program_certificate_lt_1_yr_health`: Certificate of less than one academic year in Health Professions And Related Programs.
    - `program_certificate_lt_1_yr_history`: Certificate of less than one academic year in History.
    - `program_certificate_lt_1_yr_humanities`: Certificate of less than one academic year in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_certificate_lt_1_yr_language`: Certificate of less than one academic year in Foreign Languages, Literatures, And Linguistics.
    - `program_certificate_lt_1_yr_legal`: Certificate of less than one academic year in Legal Professions And Studies.
    - `program_certificate_lt_1_yr_library`: Certificate of less than one academic year in Library Science.
    - `program_certificate_lt_1_yr_mathematics`: Certificate of less than one academic year in Mathematics And Statistics.
    - `program_certificate_lt_1_yr_mechanic_repair_technology`: Certificate of less than one academic year in Mechanic And Repair Technologies/Technicians.
    - `program_certificate_lt_1_yr_military`: Certificate of less than one academic year in Military Technologies And Applied Sciences.
    - `program_certificate_lt_1_yr_multidiscipline`: Certificate of less than one academic year in Multi/Interdisciplinary Studies.
    - `program_certificate_lt_1_yr_parks_recreation_fitness`: Certificate of less than one academic year in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_certificate_lt_1_yr_personal_culinary`: Certificate of less than one academic year in Personal And Culinary Services.
    - `program_certificate_lt_1_yr_philosophy_religious`: Certificate of less than one academic year in Philosophy And Religious Studies.
    - `program_certificate_lt_1_yr_physical_science`: Certificate of less than one academic year in Physical Sciences.
    - `program_certificate_lt_1_yr_precision_production`: Certificate of less than one academic year in Precision Production.
    - `program_certificate_lt_1_yr_psychology`: Certificate of less than one academic year in Psychology.
    - `program_certificate_lt_1_yr_public_administration_social_service`: Certificate of less than one academic year in Public Administration And Social Service Professions.
    - `program_certificate_lt_1_yr_resources`: Certificate of less than one academic year in Natural Resources And Conservation.
    - `program_certificate_lt_1_yr_science_technology`: Certificate of less than one academic year in Science Technologies/Technicians.
    - `program_certificate_lt_1_yr_security_law_enforcement`: Certificate of less than one academic year in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_certificate_lt_1_yr_social_science`: Certificate of less than one academic year in Social Sciences.
    - `program_certificate_lt_1_yr_theology_religious_vocation`: Certificate of less than one academic year in Theology And Religious Vocations.
    - `program_certificate_lt_1_yr_transportation`: Certificate of less than one academic year in Transportation And Materials Moving.
    - `program_certificate_lt_1_yr_visual_performing`: Certificate of less than one academic year in Visual And Performing Arts.
    - `program_certificate_lt_2_yr_agriculture`: Certificate of at least one but less than two academic years in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_certificate_lt_2_yr_architecture`: Certificate of at least one but less than two academic years in Architecture And Related Services.
    - `program_certificate_lt_2_yr_biological`: Certificate of at least one but less than two academic years in Biological And Biomedical Sciences.
    - `program_certificate_lt_2_yr_business_marketing`: Certificate of at least one but less than two academic years in Business, Management, Marketing, And Related Support Services.
    - `program_certificate_lt_2_yr_communication`: Certificate of at least one but less than two academic years in Communication, Journalism, And Related Programs.
    - `program_certificate_lt_2_yr_communications_technology`: Certificate of at least one but less than two academic years in Communications Technologies/Technicians And Support Services.
    - `program_certificate_lt_2_yr_computer`: Certificate of at least one but less than two academic years in Computer And Information Sciences And Support Services.
    - `program_certificate_lt_2_yr_construction`: Certificate of at least one but less than two academic years in Construction Trades.
    - `program_certificate_lt_2_yr_education`: Certificate of at least one but less than two academic years in Education.
    - `program_certificate_lt_2_yr_engineering`: Certificate of at least one but less than two academic years in Engineering.
    - `program_certificate_lt_2_yr_engineering_technology`: Certificate of at least one but less than two academic years in Engineering Technologies And Engineering-Related Fields.
    - `program_certificate_lt_2_yr_english`: Certificate of at least one but less than two academic years in English Language And Literature/Letters.
    - `program_certificate_lt_2_yr_ethnic_cultural_gender`: Certificate of at least one but less than two academic years in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_certificate_lt_2_yr_family_consumer_science`: Certificate of at least one but less than two academic years in Family And Consumer Sciences/Human Sciences.
    - `program_certificate_lt_2_yr_health`: Certificate of at least one but less than two academic years in Health Professions And Related Programs.
    - `program_certificate_lt_2_yr_history`: Certificate of at least one but less than two academic years in History.
    - `program_certificate_lt_2_yr_humanities`: Certificate of at least one but less than two academic years in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_certificate_lt_2_yr_language`: Certificate of at least one but less than two academic years in Foreign Languages, Literatures, And Linguistics.
    - `program_certificate_lt_2_yr_legal`: Certificate of at least one but less than two academic years in Legal Professions And Studies.
    - `program_certificate_lt_2_yr_library`: Certificate of at least one but less than two academic years in Library Science.
    - `program_certificate_lt_2_yr_mathematics`: Certificate of at least one but less than two academic years in Mathematics And Statistics.
    - `program_certificate_lt_2_yr_mechanic_repair_technology`: Certificate of at least one but less than two academic years in Mechanic And Repair Technologies/Technicians.
    - `program_certificate_lt_2_yr_military`: Certificate of at least one but less than two academic years in Military Technologies And Applied Sciences.
    - `program_certificate_lt_2_yr_multidiscipline`: Certificate of at least one but less than two academic years in Multi/Interdisciplinary Studies.
    - `program_certificate_lt_2_yr_parks_recreation_fitness`: Certificate of at least one but less than two academic years in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_certificate_lt_2_yr_personal_culinary`: Certificate of at least one but less than two academic years in Personal And Culinary Services.
    - `program_certificate_lt_2_yr_philosophy_religious`: Certificate of at least one but less than two academic years in Philosophy And Religious Studies.
    - `program_certificate_lt_2_yr_physical_science`: Certificate of at least one but less than two academic years in Physical Sciences.
    - `program_certificate_lt_2_yr_precision_production`: Certificate of at least one but less than two academic years in Precision Production.
    - `program_certificate_lt_2_yr_psychology`: Certificate of at least one but less than two academic years in Psychology.
    - `program_certificate_lt_2_yr_public_administration_social_service`: Certificate of at least one but less than two academic years in Public Administration And Social Service Professions.
    - `program_certificate_lt_2_yr_resources`: Certificate of at least one but less than two academic years in Natural Resources And Conservation.
    - `program_certificate_lt_2_yr_science_technology`: Certificate of at least one but less than two academic years in Science Technologies/Technicians.
    - `program_certificate_lt_2_yr_security_law_enforcement`: Certificate of at least one but less than two academic years in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_certificate_lt_2_yr_social_science`: Certificate of at least one but less than two academic years in Social Sciences.
    - `program_certificate_lt_2_yr_theology_religious_vocation`: Certificate of at least one but less than two academic years in Theology And Religious Vocations.
    - `program_certificate_lt_2_yr_transportation`: Certificate of at least one but less than two academic years in Transportation And Materials Moving.
    - `program_certificate_lt_2_yr_visual_performing`: Certificate of at least one but less than two academic years in Visual And Performing Arts.
    - `program_certificate_lt_4_yr_agriculture`: Awards of at least two but less than four academic years in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_certificate_lt_4_yr_architecture`: Award of more than two but less than four academic years in Architecture And Related Services.
    - `program_certificate_lt_4_yr_biological`: Award of more than two but less than four academic years in Biological And Biomedical Sciences.
    - `program_certificate_lt_4_yr_business_marketing`: Award of more than two but less than four academic years in Business, Management, Marketing, And Related Support Services.
    - `program_certificate_lt_4_yr_communication`: Award of more than two but less than four academic years in Communication, Journalism, And Related Programs.
    - `program_certificate_lt_4_yr_communications_technology`: Award of more than two but less than four academic years in Communications Technologies/Technicians And Support Services.
    - `program_certificate_lt_4_yr_computer`: Award of more than two but less than four academic years in Computer And Information Sciences And Support Services.
    - `program_certificate_lt_4_yr_construction`: Award of more than two but less than four academic years in Construction Trades.
    - `program_certificate_lt_4_yr_education`: Award of more than two but less than four academic years in Education.
    - `program_certificate_lt_4_yr_engineering`: Award of more than two but less than four academic years in Engineering.
    - `program_certificate_lt_4_yr_engineering_technology`: Award of more than two but less than four academic years in Engineering Technologies And Engineering-Related Fields.
    - `program_certificate_lt_4_yr_english`: Award of more than two but less than four academic years in English Language And Literature/Letters.
    - `program_certificate_lt_4_yr_ethnic_cultural_gender`: Award of more than two but less than four academic years in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_certificate_lt_4_yr_family_consumer_science`: Award of more than two but less than four academic years in Family And Consumer Sciences/Human Sciences.
    - `program_certificate_lt_4_yr_health`: Award of more than two but less than four academic years in Health Professions And Related Programs.
    - `program_certificate_lt_4_yr_history`: Award of more than two but less than four academic years in History.
    - `program_certificate_lt_4_yr_humanities`: Award of more than two but less than four academic years in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_certificate_lt_4_yr_language`: Award of more than two but less than four academic years in Foreign Languages, Literatures, And Linguistics.
    - `program_certificate_lt_4_yr_legal`: Award of more than two but less than four academic years in Legal Professions And Studies.
    - `program_certificate_lt_4_yr_library`: Award of more than two but less than four academic years in Library Science.
    - `program_certificate_lt_4_yr_mathematics`: Award of more than two but less than four academic years in Mathematics And Statistics.
    - `program_certificate_lt_4_yr_mechanic_repair_technology`: Award of more than two but less than four academic years in Mechanic And Repair Technologies/Technicians.
    - `program_certificate_lt_4_yr_military`: Award of more than two but less than four academic years in Military Technologies And Applied Sciences.
    - `program_certificate_lt_4_yr_multidiscipline`: Award of more than two but less than four academic years in Multi/Interdisciplinary Studies.
    - `program_certificate_lt_4_yr_parks_recreation_fitness`: Award of more than two but less than four academic years in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_certificate_lt_4_yr_personal_culinary`: Award of more than two but less than four academic years in Personal And Culinary Services.
    - `program_certificate_lt_4_yr_philosophy_religious`: Award of more than two but less than four academic years in Philosophy And Religious Studies.
    - `program_certificate_lt_4_yr_physical_science`: Award of more than two but less than four academic years in Physical Sciences.
    - `program_certificate_lt_4_yr_precision_production`: Award of more than two but less than four academic years in Precision Production.
    - `program_certificate_lt_4_yr_psychology`: Award of more than two but less than four academic years in Psychology.
    - `program_certificate_lt_4_yr_public_administration_social_service`: Award of more than two but less than four academic years in Public Administration And Social Service Professions.
    - `program_certificate_lt_4_yr_resources`: Award of at least two but less than four academic years in Natural Resources And Conservation.
    - `program_certificate_lt_4_yr_science_technology`: Award of more than two but less than four academic years in Science Technologies/Technicians.
    - `program_certificate_lt_4_yr_security_law_enforcement`: Award of more than two but less than four academic years in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_certificate_lt_4_yr_social_science`: Award of more than two but less than four academic years in Social Sciences.
    - `program_certificate_lt_4_yr_theology_religious_vocation`: Award of more than two but less than four academic years in Theology And Religious Vocations.
    - `program_certificate_lt_4_yr_transportation`: Award of more than two but less than four academic years in Transportation And Materials Moving.
    - `program_certificate_lt_4_yr_visual_performing`: Award of more than two but less than four academic years in Visual And Performing Arts.
    - `program_percentage_agriculture`: Percentage of degrees awarded in Agriculture, Agriculture Operations, And Related Sciences.
    - `program_percentage_architecture`: Percentage of degrees awarded in Architecture And Related Services.
    - `program_percentage_biological`: Percentage of degrees awarded in Biological And Biomedical Sciences.
    - `program_percentage_business_marketing`: Percentage of degrees awarded in Business, Management, Marketing, And Related Support Services.
    - `program_percentage_communication`: Percentage of degrees awarded in Communication, Journalism, And Related Programs.
    - `program_percentage_communications_technology`: Percentage of degrees awarded in Communications Technologies/Technicians And Support Services.
    - `program_percentage_computer`: Percentage of degrees awarded in Computer And Information Sciences And Support Services.
    - `program_percentage_construction`: Percentage of degrees awarded in Construction Trades.
    - `program_percentage_education`: Percentage of degrees awarded in Education.
    - `program_percentage_engineering`: Percentage of degrees awarded in Engineering.
    - `program_percentage_engineering_technology`: Percentage of degrees awarded in Engineering Technologies And Engineering-Related Fields.
    - `program_percentage_english`: Percentage of degrees awarded in English Language And Literature/Letters.
    - `program_percentage_ethnic_cultural_gender`: Percentage of degrees awarded in Area, Ethnic, Cultural, Gender, And Group Studies.
    - `program_percentage_family_consumer_science`: Percentage of degrees awarded in Family And Consumer Sciences/Human Sciences.
    - `program_percentage_health`: Percentage of degrees awarded in Health Professions And Related Programs.
    - `program_percentage_history`: Percentage of degrees awarded in History.
    - `program_percentage_humanities`: Percentage of degrees awarded in Liberal Arts And Sciences, General Studies And Humanities.
    - `program_percentage_language`: Percentage of degrees awarded in Foreign Languages, Literatures, And Linguistics.
    - `program_percentage_legal`: Percentage of degrees awarded in Legal Professions And Studies.
    - `program_percentage_library`: Percentage of degrees awarded in Library Science.
    - `program_percentage_mathematics`: Percentage of degrees awarded in Mathematics And Statistics.
    - `program_percentage_mechanic_repair_technology`: Percentage of degrees awarded in Mechanic And Repair Technologies/Technicians.
    - `program_percentage_military`: Percentage of degrees awarded in Military Technologies And Applied Sciences.
    - `program_percentage_multidiscipline`: Percentage of degrees awarded in Multi/Interdisciplinary Studies.
    - `program_percentage_parks_recreation_fitness`: Percentage of degrees awarded in Parks, Recreation, Leisure, And Fitness Studies.
    - `program_percentage_personal_culinary`: Percentage of degrees awarded in Personal And Culinary Services.
    - `program_percentage_philosophy_religious`: Percentage of degrees awarded in Philosophy And Religious Studies.
    - `program_percentage_physical_science`: Percentage of degrees awarded in Physical Sciences.
    - `program_percentage_precision_production`: Percentage of degrees awarded in Precision Production.
    - `program_percentage_psychology`: Percentage of degrees awarded in Psychology.
    - `program_percentage_public_administration_social_service`: Percentage of degrees awarded in Public Administration And Social Service Professions.
    - `program_percentage_resources`: Percentage of degrees awarded in Natural Resources And Conservation.
    - `program_percentage_science_technology`: Percentage of degrees awarded in Science Technologies/Technicians.
    - `program_percentage_security_law_enforcement`: Percentage of degrees awarded in Homeland Security, Law Enforcement, Firefighting And Related Protective Services.
    - `program_percentage_social_science`: Percentage of degrees awarded in Social Sciences.
    - `program_percentage_theology_religious_vocation`: Percentage of degrees awarded in Theology And Religious Vocations.
    - `program_percentage_transportation`: Percentage of degrees awarded in Transportation And Materials Moving.
    - `program_percentage_visual_performing`: Percentage of degrees awarded in Visual And Performing Arts.

 - **`admissions`**

    - `act_scores_25th_percentile_cumulative`: 25th percentile of the ACT cumulative score
    - `act_scores_25th_percentile_english`: 25th percentile of the ACT English score
    - `act_scores_25th_percentile_math`: 25th percentile of the ACT math score
    - `act_scores_25th_percentile_writing`: 25th percentile of the ACT writing score
    - `act_scores_75th_percentile_cumulative`: 75th percentile of the ACT cumulative score
    - `act_scores_75th_percentile_english`: 75th percentile of the ACT English score
    - `act_scores_75th_percentile_math`: 75th percentile of the ACT math score
    - `act_scores_75th_percentile_writing`: 75th percentile of the ACT writing score
    - `act_scores_midpoint_cumulative`: Midpoint of the ACT cumulative score
    - `act_scores_midpoint_english`: Midpoint of the ACT English score
    - `act_scores_midpoint_math`: Midpoint of the ACT math score
    - `act_scores_midpoint_writing`: Midpoint of the ACT writing score
    - `admission_rate_by_ope_id`: Admission rate for all campuses rolled up to the 6-digit OPE ID
    - `admission_rate_overall`: Admission rate
    - `sat_scores_25th_percentile_critical_reading`: 25th percentile of SAT scores at the institution (critical reading)
    - `sat_scores_25th_percentile_math`: 25th percentile of SAT scores at the institution (math)
    - `sat_scores_25th_percentile_writing`: 25th percentile of SAT scores at the institution (writing)
    - `sat_scores_75th_percentile_critical_reading`: 75th percentile of SAT scores at the institution (critical reading)
    - `sat_scores_75th_percentile_math`: 75th percentile of SAT scores at the institution (math)
    - `sat_scores_75th_percentile_writing`: 75th percentile of SAT scores at the institution (writing)
    - `sat_scores_average_by_ope_id`: Average SAT equivalent score of students admitted for all campuses rolled up to the 6-digit OPE ID
    - `sat_scores_average_overall`: Average SAT equivalent score of students admitted
    - `sat_scores_midpoint_critical_reading`: Midpoint of SAT scores at the institution (critical reading)
    - `sat_scores_midpoint_math`: Midpoint of SAT scores at the institution (math)
    - `sat_scores_midpoint_writing`: Midpoint of SAT scores at the institution (writing)

 - **`completion`**

    - `completion_cohort_4yr_100nt`: Adjusted cohort count for completion rate at four-year institutions (denominator of 100% completion rate)
    - `completion_cohort_less_than_4yr_100nt`: Adjusted cohort count for completion rate at less-than-four-year institutions (denominator of 100% completion rate)
    - `completion_rate_4yr_100nt`: Completion rate for first-time, full-time students at four-year institutions (100% of expected time to completion/6 years)
    - `completion_rate_less_than_4yr_100nt`: Completion rate for first-time, full-time students at less-than-four-year institutions (100% of expected time to completion)
    - `transfer_rate_4yr_full_time`: Transfer rate for first-time, full-time students at four-year institutions (within 150% of expected time to completion/6 years)
    - `transfer_rate_cohort_4yr_full_time`: Adjusted cohort count for transfer rate at less-than-four-year institutions (denominator of 150% transfer rate)
    - `transfer_rate_cohort_less_than_4yr_full_time`: Adjusted cohort count for transfer rate at four-year institutions (denominator of 150% transfer rate)
    - `transfer_rate_less_than_4yr_full_time`: Transfer rate for first-time, full-time students at less-than-four-year institutions (150% of expected time to completion)

 - **`cost`**

    - `tuition_in_state`: In-state tuition and fees
    - `tuition_out_of_state`: Out-of-state tuition and fees
    - `tuition_program_year`: Tuition and fees for program-year institutions

 - **`year`**

    - `report_year`: A variable indicating what year the observation is from. (Possible Values: `year_a`, `year_f`, `year_z`, `year_w`)

 - **`school`**

    - `degrees_awarded_highest`: Highest degree awarded
 0 Non-degree-granting
 1 Certificate degree
 2 Associate degree
 3 Bachelor's degree
 4 Graduate degree (Possible Values: `Associate degree`, `Graduate degree`, `Certificate degree`, `Bachelor's degree`, `Non-degree-granting`)
    - `degrees_awarded_predominant`: Predominant undergraduate degree awarded
 0 Not classified
 1 Predominantly certificate-degree granting
 2 Predominantly associate's-degree granting
 3 Predominantly bachelor's-degree granting
 4 Entirely graduate-degree granting (Possible Values: `Predominantly certificate-degree granting`, `Predominantly bachelor's-degree granting`, `Predominantly associate's-degree granting`, `Not classified`, `Entirely graduate-degree granting`)
    - `degrees_awarded_predominant_recoded`: Predominant degree awarded (recoded 0s and 4s)
    - `faculty_salary`: Average faculty salary
    - `ft_faculty_rate`: Proportion of faculty that is full-time
    - `institutional_characteristics_level`: Level of institution (Possible Values: `2-year`, `4-year`, `Less-than-2-year`)
    - `instructional_expenditure_per_fte`: Instructional expenditures per full-time equivalent student
    - `main_campus`: Flag for main campus (Possible Values: `Main campus`, `Not main campus`)
    - `online_only`: Flag for distance-education-only education (Possible Values: `Not distance-education only`, `nan`, `Distance-education only`)
    - `ownership`: Control of institution (Possible Values: `Public`, `Private for-profit`, `Private nonprofit`)
    - `region_id`: Region (IPEDS) (Possible Values: `Plains (IA, KS, MN, MO, NE, ND, SD)`, `New England (CT, ME, MA, NH, RI, VT)`, `Southeast (AL, AR, FL, GA, KY, LA, MS, NC, SC, TN, VA, WV)`, `Mid East (DE, DC, MD, NJ, NY, PA)`, `Great Lakes (IL, IN, MI, OH, WI)`, `Far West (AK, CA, HI, NV, OR, WA)`, `Southwest (AZ, NM, OK, TX)`, `Rocky Mountains (CO, ID, MT, UT, WY)`, `Outlying Areas (AS, FM, GU, MH, MP, PR, PW, VI)`)
    - `state`: State postcode (Possible Values: `axc`, `fga`, `oly`, `dmg`, `hbt`, `jgn`, `kll`, `xve`, `dfy`, `oon`, `oli`, `iqy`, `qim`, `shi`, `ccg`, `dkf`, `ipu`, `tbs`, `luw`, `pxv`, `hww`, `lff`, `slp`, `wjh`, `idw`, `ezv`, `vvi`, `zdl`, `jsu`, `hks`, `bww`, `fxt`, `rxy`, `cfi`, `rse`, `kus`, `oub`, `uah`, `rya`, `eyi`, `wto`, `gkt`, `bkc`, `znt`, `slo`, `hqy`, `rgs`, `cmz`, `kdg`, `pdh`, `ahh`, `twr`, `xws`, `por`, `uuo`, `nhl`, `hmr`, `jfm`)
    - `tuition_revenue_per_fte`: Net tuition revenue per full-time equivalent student

 - **`student`**

    - `demographics_age_entry`: Average age of entry, via SSA data
    - `demographics_dependent`: Share of dependent students
    - `demographics_female_share`: Share of female students, via SSA data
    - `demographics_first_generation`: Share of first-generation students
    - `demographics_married`: Share of married students
    - `demographics_veteran`: Share of veteran students
    - `part_time_share`: Share of undergraduate, degree-/certificate-seeking students who are part-time
    - `retention_rate_four_year_full_time`: First-time, full-time student retention rate at four-year institutions
    - `retention_rate_four_year_part_time`: First-time, part-time student retention rate at four-year institutions
    - `retention_rate_lt_four_year_full_time`: First-time, full-time student retention rate at less-than-four-year institutions
    - `retention_rate_lt_four_year_part_time`: First-time, part-time student retention rate at less-than-four-year institutions
    - `share_25_older`: Percentage of undergraduates aged 25 and above
    - `share_first_time_full_time`: Share of undergraduate students who are first-time, full-time degree-/certificate-seeking undergraduate students
    - `share_firstgeneration`: Percentage first-generation students
    - `share_firstgeneration_parents_highschool`: Percent of students whose parents' highest educational level is high school
    - `share_firstgeneration_parents_middleschool`: Percent of students whose parents' highest educational level is middle school
    - `share_firstgeneration_parents_somecollege`: Percent of students whose parents' highest educational level was is some form of postsecondary education
    - `share_independent_students`: Percentage of students who are financially independent
    - `size`: Enrollment of undergraduate certificate/degree-seeking students

<a id="example-row"></a>

### Example Row

Here's an example of one of the rows in the dataset so that you can see the kinds of values you might expect in the dataset. Some are numeric, some are categorical, and there are often missing values.

| field                                                                                  | value          |
|----------------------------------------------------------------------------------------|----------------|
| academics__program_assoc_agriculture | 0.0 |
| academics__program_assoc_architecture | 0.0 |
| academics__program_assoc_biological | 0.0 |
| academics__program_assoc_business_marketing | 0.0 |
| academics__program_assoc_communication | 0.0 |
| academics__program_assoc_communications_technology | 0.0 |
| academics__program_assoc_computer | 0.0 |
| academics__program_assoc_construction | 0.0 |
| academics__program_assoc_education | 0.0 |
| academics__program_assoc_engineering | 0.0 |
| academics__program_assoc_engineering_technology | 0.0 |
| academics__program_assoc_english | 0.0 |
| academics__program_assoc_ethnic_cultural_gender | 0.0 |
| academics__program_assoc_family_consumer_science | 0.0 |
| academics__program_assoc_health | 0.0 |
| academics__program_assoc_history | 0.0 |
| academics__program_assoc_humanities | 0.0 |
| academics__program_assoc_language | 0.0 |
| academics__program_assoc_legal | 0.0 |
| academics__program_assoc_library | 0.0 |
| academics__program_assoc_mathematics | 0.0 |
| academics__program_assoc_mechanic_repair_technology | 0.0 |
| academics__program_assoc_military | 0.0 |
| academics__program_assoc_multidiscipline | 0.0 |
| academics__program_assoc_parks_recreation_fitness | 0.0 |
| academics__program_assoc_personal_culinary | 0.0 |
| academics__program_assoc_philosophy_religious | 0.0 |
| academics__program_assoc_physical_science | 0.0 |
| academics__program_assoc_precision_production | 0.0 |
| academics__program_assoc_psychology | 0.0 |
| academics__program_assoc_public_administration_social_service | 0.0 |
| academics__program_assoc_resources | 0.0 |
| academics__program_assoc_science_technology | 0.0 |
| academics__program_assoc_security_law_enforcement | 0.0 |
| academics__program_assoc_social_science | 0.0 |
| academics__program_assoc_theology_religious_vocation | 0.0 |
| academics__program_assoc_transportation | 0.0 |
| academics__program_assoc_visual_performing | 0.0 |
| academics__program_bachelors_agriculture | 0.0 |
| academics__program_bachelors_architecture | 0.0 |
| academics__program_bachelors_biological | 0.0 |
| academics__program_bachelors_business_marketing | 0.0 |
| academics__program_bachelors_communication | 0.0 |
| academics__program_bachelors_communications_technology | 0.0 |
| academics__program_bachelors_computer | 0.0 |
| academics__program_bachelors_construction | 0.0 |
| academics__program_bachelors_education | 0.0 |
| academics__program_bachelors_engineering | 0.0 |
| academics__program_bachelors_engineering_technology | 0.0 |
| academics__program_bachelors_english | 0.0 |
| academics__program_bachelors_ethnic_cultural_gender | 0.0 |
| academics__program_bachelors_family_consumer_science | 0.0 |
| academics__program_bachelors_health | 0.0 |
| academics__program_bachelors_history | 0.0 |
| academics__program_bachelors_humanities | 0.0 |
| academics__program_bachelors_language | 0.0 |
| academics__program_bachelors_legal | 0.0 |
| academics__program_bachelors_library | 0.0 |
| academics__program_bachelors_mathematics | 0.0 |
| academics__program_bachelors_mechanic_repair_technology | 0.0 |
| academics__program_bachelors_military | 0.0 |
| academics__program_bachelors_multidiscipline | 0.0 |
| academics__program_bachelors_parks_recreation_fitness | 0.0 |
| academics__program_bachelors_personal_culinary | 0.0 |
| academics__program_bachelors_philosophy_religious | 0.0 |
| academics__program_bachelors_physical_science | 0.0 |
| academics__program_bachelors_precision_production | 0.0 |
| academics__program_bachelors_psychology | 0.0 |
| academics__program_bachelors_public_administration_social_service | 0.0 |
| academics__program_bachelors_resources | 0.0 |
| academics__program_bachelors_science_technology | 0.0 |
| academics__program_bachelors_security_law_enforcement | 0.0 |
| academics__program_bachelors_social_science | 0.0 |
| academics__program_bachelors_theology_religious_vocation | 0.0 |
| academics__program_bachelors_transportation | 0.0 |
| academics__program_bachelors_visual_performing | 0.0 |
| academics__program_certificate_lt_1_yr_agriculture | 0.0 |
| academics__program_certificate_lt_1_yr_architecture | 0.0 |
| academics__program_certificate_lt_1_yr_biological | 0.0 |
| academics__program_certificate_lt_1_yr_business_marketing | 0.0 |
| academics__program_certificate_lt_1_yr_communication | 0.0 |
| academics__program_certificate_lt_1_yr_communications_technology | 0.0 |
| academics__program_certificate_lt_1_yr_computer | 0.0 |
| academics__program_certificate_lt_1_yr_construction | 0.0 |
| academics__program_certificate_lt_1_yr_education | 0.0 |
| academics__program_certificate_lt_1_yr_engineering | 0.0 |
| academics__program_certificate_lt_1_yr_engineering_technology | 0.0 |
| academics__program_certificate_lt_1_yr_english | 0.0 |
| academics__program_certificate_lt_1_yr_ethnic_cultural_gender | 0.0 |
| academics__program_certificate_lt_1_yr_family_consumer_science | 0.0 |
| academics__program_certificate_lt_1_yr_health | 0.0 |
| academics__program_certificate_lt_1_yr_history | 0.0 |
| academics__program_certificate_lt_1_yr_humanities | 0.0 |
| academics__program_certificate_lt_1_yr_language | 0.0 |
| academics__program_certificate_lt_1_yr_legal | 0.0 |
| academics__program_certificate_lt_1_yr_library | 0.0 |
| academics__program_certificate_lt_1_yr_mathematics | 0.0 |
| academics__program_certificate_lt_1_yr_mechanic_repair_technology | 0.0 |
| academics__program_certificate_lt_1_yr_military | 0.0 |
| academics__program_certificate_lt_1_yr_multidiscipline | 0.0 |
| academics__program_certificate_lt_1_yr_parks_recreation_fitness | 0.0 |
| academics__program_certificate_lt_1_yr_personal_culinary | 0.0 |
| academics__program_certificate_lt_1_yr_philosophy_religious | 0.0 |
| academics__program_certificate_lt_1_yr_physical_science | 0.0 |
| academics__program_certificate_lt_1_yr_precision_production | 0.0 |
| academics__program_certificate_lt_1_yr_psychology | 0.0 |
| academics__program_certificate_lt_1_yr_public_administration_social_service | 0.0 |
| academics__program_certificate_lt_1_yr_resources | 0.0 |
| academics__program_certificate_lt_1_yr_science_technology | 0.0 |
| academics__program_certificate_lt_1_yr_security_law_enforcement | 0.0 |
| academics__program_certificate_lt_1_yr_social_science | 0.0 |
| academics__program_certificate_lt_1_yr_theology_religious_vocation | 0.0 |
| academics__program_certificate_lt_1_yr_transportation | 0.0 |
| academics__program_certificate_lt_1_yr_visual_performing | 0.0 |
| academics__program_certificate_lt_2_yr_agriculture | 0.0 |
| academics__program_certificate_lt_2_yr_architecture | 0.0 |
| academics__program_certificate_lt_2_yr_biological | 0.0 |
| academics__program_certificate_lt_2_yr_business_marketing | 0.0 |
| academics__program_certificate_lt_2_yr_communication | 0.0 |
| academics__program_certificate_lt_2_yr_communications_technology | 0.0 |
| academics__program_certificate_lt_2_yr_computer | 0.0 |
| academics__program_certificate_lt_2_yr_construction | 0.0 |
| academics__program_certificate_lt_2_yr_education | 0.0 |
| academics__program_certificate_lt_2_yr_engineering | 0.0 |
| academics__program_certificate_lt_2_yr_engineering_technology | 0.0 |
| academics__program_certificate_lt_2_yr_english | 0.0 |
| academics__program_certificate_lt_2_yr_ethnic_cultural_gender | 0.0 |
| academics__program_certificate_lt_2_yr_family_consumer_science | 0.0 |
| academics__program_certificate_lt_2_yr_health | 0.0 |
| academics__program_certificate_lt_2_yr_history | 0.0 |
| academics__program_certificate_lt_2_yr_humanities | 0.0 |
| academics__program_certificate_lt_2_yr_language | 0.0 |
| academics__program_certificate_lt_2_yr_legal | 0.0 |
| academics__program_certificate_lt_2_yr_library | 0.0 |
| academics__program_certificate_lt_2_yr_mathematics | 0.0 |
| academics__program_certificate_lt_2_yr_mechanic_repair_technology | 0.0 |
| academics__program_certificate_lt_2_yr_military | 0.0 |
| academics__program_certificate_lt_2_yr_multidiscipline | 0.0 |
| academics__program_certificate_lt_2_yr_parks_recreation_fitness | 0.0 |
| academics__program_certificate_lt_2_yr_personal_culinary | 0.0 |
| academics__program_certificate_lt_2_yr_philosophy_religious | 0.0 |
| academics__program_certificate_lt_2_yr_physical_science | 0.0 |
| academics__program_certificate_lt_2_yr_precision_production | 0.0 |
| academics__program_certificate_lt_2_yr_psychology | 0.0 |
| academics__program_certificate_lt_2_yr_public_administration_social_service | 0.0 |
| academics__program_certificate_lt_2_yr_resources | 0.0 |
| academics__program_certificate_lt_2_yr_science_technology | 0.0 |
| academics__program_certificate_lt_2_yr_security_law_enforcement | 0.0 |
| academics__program_certificate_lt_2_yr_social_science | 0.0 |
| academics__program_certificate_lt_2_yr_theology_religious_vocation | 0.0 |
| academics__program_certificate_lt_2_yr_transportation | 0.0 |
| academics__program_certificate_lt_2_yr_visual_performing | 0.0 |
| academics__program_certificate_lt_4_yr_agriculture | 0.0 |
| academics__program_certificate_lt_4_yr_architecture | 0.0 |
| academics__program_certificate_lt_4_yr_biological | 0.0 |
| academics__program_certificate_lt_4_yr_business_marketing | 0.0 |
| academics__program_certificate_lt_4_yr_communication | 0.0 |
| academics__program_certificate_lt_4_yr_communications_technology | 0.0 |
| academics__program_certificate_lt_4_yr_computer | 0.0 |
| academics__program_certificate_lt_4_yr_construction | 0.0 |
| academics__program_certificate_lt_4_yr_education | 0.0 |
| academics__program_certificate_lt_4_yr_engineering | 0.0 |
| academics__program_certificate_lt_4_yr_engineering_technology | 0.0 |
| academics__program_certificate_lt_4_yr_english | 0.0 |
| academics__program_certificate_lt_4_yr_ethnic_cultural_gender | 0.0 |
| academics__program_certificate_lt_4_yr_family_consumer_science | 0.0 |
| academics__program_certificate_lt_4_yr_health | 1.0 |
| academics__program_certificate_lt_4_yr_history | 0.0 |
| academics__program_certificate_lt_4_yr_humanities | 0.0 |
| academics__program_certificate_lt_4_yr_language | 0.0 |
| academics__program_certificate_lt_4_yr_legal | 0.0 |
| academics__program_certificate_lt_4_yr_library | 0.0 |
| academics__program_certificate_lt_4_yr_mathematics | 0.0 |
| academics__program_certificate_lt_4_yr_mechanic_repair_technology | 0.0 |
| academics__program_certificate_lt_4_yr_military | 0.0 |
| academics__program_certificate_lt_4_yr_multidiscipline | 0.0 |
| academics__program_certificate_lt_4_yr_parks_recreation_fitness | 0.0 |
| academics__program_certificate_lt_4_yr_personal_culinary | 0.0 |
| academics__program_certificate_lt_4_yr_philosophy_religious | 0.0 |
| academics__program_certificate_lt_4_yr_physical_science | 0.0 |
| academics__program_certificate_lt_4_yr_precision_production | 0.0 |
| academics__program_certificate_lt_4_yr_psychology | 0.0 |
| academics__program_certificate_lt_4_yr_public_administration_social_service | 0.0 |
| academics__program_certificate_lt_4_yr_resources | 0.0 |
| academics__program_certificate_lt_4_yr_science_technology | 0.0 |
| academics__program_certificate_lt_4_yr_security_law_enforcement | 0.0 |
| academics__program_certificate_lt_4_yr_social_science | 0.0 |
| academics__program_certificate_lt_4_yr_theology_religious_vocation | 0.0 |
| academics__program_certificate_lt_4_yr_transportation | 0.0 |
| academics__program_certificate_lt_4_yr_visual_performing | 0.0 |
| academics__program_percentage_agriculture | 0.0 |
| academics__program_percentage_architecture | 0.0 |
| academics__program_percentage_biological | 0.0 |
| academics__program_percentage_business_marketing | 0.0 |
| academics__program_percentage_communication | 0.0 |
| academics__program_percentage_communications_technology | 0.0 |
| academics__program_percentage_computer | 0.0 |
| academics__program_percentage_construction | 0.0 |
| academics__program_percentage_education | 0.0 |
| academics__program_percentage_engineering | 0.0 |
| academics__program_percentage_engineering_technology | 0.0 |
| academics__program_percentage_english | 0.0 |
| academics__program_percentage_ethnic_cultural_gender | 0.0 |
| academics__program_percentage_family_consumer_science | 0.0 |
| academics__program_percentage_health | 1.0 |
| academics__program_percentage_history | 0.0 |
| academics__program_percentage_humanities | 0.0 |
| academics__program_percentage_language | 0.0 |
| academics__program_percentage_legal | 0.0 |
| academics__program_percentage_library | 0.0 |
| academics__program_percentage_mathematics | 0.0 |
| academics__program_percentage_mechanic_repair_technology | 0.0 |
| academics__program_percentage_military | 0.0 |
| academics__program_percentage_multidiscipline | 0.0 |
| academics__program_percentage_parks_recreation_fitness | 0.0 |
| academics__program_percentage_personal_culinary | 0.0 |
| academics__program_percentage_philosophy_religious | 0.0 |
| academics__program_percentage_physical_science | 0.0 |
| academics__program_percentage_precision_production | 0.0 |
| academics__program_percentage_psychology | 0.0 |
| academics__program_percentage_public_administration_social_service | 0.0 |
| academics__program_percentage_resources | 0.0 |
| academics__program_percentage_science_technology | 0.0 |
| academics__program_percentage_security_law_enforcement | 0.0 |
| academics__program_percentage_social_science | 0.0 |
| academics__program_percentage_theology_religious_vocation | 0.0 |
| academics__program_percentage_transportation | 0.0 |
| academics__program_percentage_visual_performing | 0.0 |
| admissions__act_scores_25th_percentile_cumulative | nan |
| admissions__act_scores_25th_percentile_english | nan |
| admissions__act_scores_25th_percentile_math | nan |
| admissions__act_scores_25th_percentile_writing | nan |
| admissions__act_scores_75th_percentile_cumulative | nan |
| admissions__act_scores_75th_percentile_english | nan |
| admissions__act_scores_75th_percentile_math | nan |
| admissions__act_scores_75th_percentile_writing | nan |
| admissions__act_scores_midpoint_cumulative | nan |
| admissions__act_scores_midpoint_english | nan |
| admissions__act_scores_midpoint_math | nan |
| admissions__act_scores_midpoint_writing | nan |
| admissions__admission_rate_by_ope_id | nan |
| admissions__admission_rate_overall | nan |
| admissions__sat_scores_25th_percentile_critical_reading | nan |
| admissions__sat_scores_25th_percentile_math | nan |
| admissions__sat_scores_25th_percentile_writing | nan |
| admissions__sat_scores_75th_percentile_critical_reading | nan |
| admissions__sat_scores_75th_percentile_math | nan |
| admissions__sat_scores_75th_percentile_writing | nan |
| admissions__sat_scores_average_by_ope_id | nan |
| admissions__sat_scores_average_overall | nan |
| admissions__sat_scores_midpoint_critical_reading | nan |
| admissions__sat_scores_midpoint_math | nan |
| admissions__sat_scores_midpoint_writing | nan |
| completion__completion_cohort_4yr_100nt | nan |
| completion__completion_cohort_less_than_4yr_100nt | nan |
| completion__completion_rate_4yr_100nt | nan |
| completion__completion_rate_less_than_4yr_100nt | nan |
| completion__transfer_rate_4yr_full_time | nan |
| completion__transfer_rate_cohort_4yr_full_time | nan |
| completion__transfer_rate_cohort_less_than_4yr_full_time | nan |
| completion__transfer_rate_less_than_4yr_full_time | nan |
| cost__tuition_in_state | nan |
| cost__tuition_out_of_state | nan |
| cost__tuition_program_year | nan |
| report_year | year_a |
| school__degrees_awarded_highest | Certificate degree |
| school__degrees_awarded_predominant | Predominantly certificate-degree granting |
| school__degrees_awarded_predominant_recoded | 1 |
| school__faculty_salary | nan |
| school__ft_faculty_rate | nan |
| school__institutional_characteristics_level | 2-year |
| school__instructional_expenditure_per_fte | 8294.0 |
| school__main_campus | Not main campus |
| school__online_only | Not distance-education only |
| school__ownership | Private nonprofit |
| school__region_id | Southeast (AL, AR, FL, GA, KY, LA, MS, NC, SC, TN, VA, WV) |
| school__state | slp |
| school__tuition_revenue_per_fte | 7736.0 |
| student__demographics_age_entry | 26.975308641999998 |
| student__demographics_dependent | 0.2716049383 |
| student__demographics_female_share | nan |
| student__demographics_first_generation | nan |
| student__demographics_married | 0.2469135802 |
| student__demographics_veteran | nan |
| student__part_time_share | 0.0 |
| student__retention_rate_four_year_full_time | nan |
| student__retention_rate_four_year_part_time | nan |
| student__retention_rate_lt_four_year_full_time | nan |
| student__retention_rate_lt_four_year_part_time | nan |
| student__share_25_older | nan |
| student__share_first_time_full_time | nan |
| student__share_firstgeneration | nan |
| student__share_firstgeneration_parents_highschool | nan |
| student__share_firstgeneration_parents_middleschool | nan |
| student__share_firstgeneration_parents_somecollege | nan |
| student__share_independent_students | 0.7283950617 |
| student__size | 56.0 |

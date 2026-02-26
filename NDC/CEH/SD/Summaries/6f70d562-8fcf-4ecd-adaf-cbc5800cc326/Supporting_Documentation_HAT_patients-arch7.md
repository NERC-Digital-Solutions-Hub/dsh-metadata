# Economic and Social Impact of Human African Trypanosomiasis (HAT) in Eastern Zambia (2004–2014)

- Overview
  - Two datasets collected to determine the economic and social consequences of HAT in Eastern Zambia.
  - Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); funded by NERC (NE/J000701/1) with ESPA support.
  - Data collected from former and current HAT patients and health workers/family members between 2004 and 2014.
  - Anonymised data: names of villages removed; verbal consent obtained; transcripts anonymised to protect individuals.

- Datasets
  - Dataset 1: HAT_Burden_DDDAC_2016.csv
    - Economic and social impact data, plus demographics, culture, and treatment-seeking information.
    - Variables include: Id, Province, District, Dist_value, Age, Sex, Marital_status, Occupation, Family_n, Formal_n, Informal_n, Unemployed_n, Income, HAT_knowledge, HAT_transmission, HAT_contact, HAT_HH, Patient_signs, Abnorm_sleep, Fever, Body_pain, Headache, LN_enlarge, Weight_loss, Paralysis, Other_symptoms, Date_symptoms, Clinic_visit, No_action, Healer, Self_med, Transport_cost, Medication_cost, Meals_cost, Washing_paste, Food_cost, Hospitalisation, Debt_accum, Debt_value, Debt_clear, Productive_work, Absent_work, Attend_school, Absent_school, School_time, School_stop, School_rpt, Hosp_disch, Disab_disch, Temper, Swelling, Mental_disor, Pain_disch, Weakness_disch, Paralysis_disch, Other_disch, Staged, Review, Review_date, Mortality, Mortality_date, Family_outlive, Child_outlive, Spouse_outlive, Parents_outlive, Depend_outlive, Recovery_full, Recovery_date, Recovery_minor, Recovery_mdate, Recovery_mental, Mental_date, Recovery_major, Major_date, Report_death, Unreport_death, Miscarriage, Suicide, Suicide_date
    - Data notes: Missing data coded with *; NA for not applicable; exchange rate data: US$1 ≈ ZMW 6.3.
  - Dataset 2: Focus group transcripts (RTF)
    - Anonymised transcripts from eight focus group discussions with health workers, people affected by HAT, and relatives/friends.
    - Data analyzed with inductive thematic coding by two independent researchers.
    - Transcripts stored as Rich Text Format (rtf) and anonymised for Environmental Information Data Centre (EIDC).

- Data collection and lineage
  - Participants: Previous and current HAT patients recruited from areas where HAT occurs in Zambia (Lusaka, Eastern, Muchinga Provinces).
  - Case confirmation: Active cases confirmed by PCR and/or LAMP; old cases via hospital or community records.
  - Data collection instruments: Structured questionnaires administered to patients or their caregivers; focus group discussions conducted by experienced University of Zambia researchers.
  - Data handling: Questionnaires compiled into Excel and exported as CSV; village names removed to anonymise; FG transcripts anonymised; data stored at the University of Zambia and converted to RTF for EIDC.

- Household Questionnaire (instrument behind Dataset 1)
  - Structure:
    - Section One: Demographic Information (age, sex, marital status, occupation, family size, employment status, approximate monthly household income)
    - Section Two: Knowledge about HAT/HAT (awareness, transmission, person-to-person transmission)
    - Section Three: Economic and Social Impact (expenditures on transport, medication, meals, washing paste, other foods; time spent at clinics; coping strategies like selling items or incurring debt; impact on productive work and schooling; hospital discharge outcomes; follow-up; mortality)
  - Key fields: Enrollment ID, Household Number, Cluster, Province/District, occupation categories, income, expenditure items, debt details, school absenteeism, hospitalisation, disabilities, recovery status.

- GIS relevance and data quality
  - Spatial components: Province and District provide coarse geographic granularity suitable for district-level mapping and spatial summaries of economic and social burden.
  - Limitations: No precise geocoordinates provided; district-level resolution may limit fine-grained spatial analysis; missing data markers present in Dataset 1.

- Ethics
  - Verbal consent obtained for all questionnaires and interviews.
  - Personal identifiers removed; data prepared to protect patient confidentiality.

- Data provenance and access notes
  - Data collected as part of a large, collaborative project (DDDAC); contributors and roles listed (design, implementation, data management and supervision).
  - Data processing steps: questionnaires to CSV; transcripts to anonymised Word/RTF formats; storage and sharing prepared for EIDC.

- Practical use for GIS Specialists
  - Enables mapping of economic and social impact of HAT across districts in Eastern Zambia.
  - Allows integration with other spatial datasets (e.g., health facilities, population, transport networks) to explore correlations between disease burden and access to care.
  - Provides a structured dataset with demographic, economic, and health-related variables suitable for spatial analysis, thematic mapping, and burden assessment at district/province levels.
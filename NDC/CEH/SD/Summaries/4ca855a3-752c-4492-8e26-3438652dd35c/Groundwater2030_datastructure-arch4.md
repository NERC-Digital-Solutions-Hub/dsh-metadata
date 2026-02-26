# Groundwater2030: Data structure for field survey files

- Purpose: Defines how four CSV tables (sanitary risk, water quality, well owner survey, well customer survey) are structured and joined using common identifiers, forming a linked data set for groundwater sources used in fieldwork.

- Data files and key fields:
  - Groundwater2030_sanrisk.csv: Description – Sanitary risk inspection of groundwater sources; Well ID field = Wellcode; primary key for this table.
  - Groundwater2030_waterquality.csv: Description – Water quality test results; Well ID field = Wellcode; primary key for this table.
  - Groundwater2030_well_owner_survey.csv: Description – Questionnaire survey of well owners; Well ID field = Well number; primary key for this table.
  - Groundwater2030_WellCustomerSurvey.csv: Description – Questionnaire survey of well customers; Well ID field = Well number; primary key for this table.

- Identifier system and data relationships:
  - Unique identifiers take the form W1…n (well), S1…n (spring), B1…n (borehole).
  - Prefix indicates source type: W = well, S = spring, B = borehole.
  - An additional code O indicates wells in the baseline survey without currently collected water quality data.
  - For owner or customer questionnaires not linked to a specific well, labels are 'None' followed by a number (1-n).
  - All questionnaires include neighbourhood information.

- Linkage and data integration:
  - Tables join on well-related identifiers: Wellcode for sanrisk and waterquality; Well number for owner and customer surveys.
  - There may be more than one customer per groundwater source, reflecting multiple links in the WellCustomerSurvey data.

- Data quality and governance considerations:
  - Ensure consistent use of identifiers across tables to maintain referential integrity.
  - Handle cases where links are missing or labeled None1, None2, etc.
  - Manage metadata to capture the meaning of O codes and the interpretation of prefixes W, S, B.

- Practical guidance for data leaders:
  - Use a master index to track all groundwater sources (W/S/B) and their associated records across the four tables.
  - Validate cross-table linkages during data ingestion and prior to analysis.
  - Be mindful of potential multiple customer records per source when performing analyses or reporting.
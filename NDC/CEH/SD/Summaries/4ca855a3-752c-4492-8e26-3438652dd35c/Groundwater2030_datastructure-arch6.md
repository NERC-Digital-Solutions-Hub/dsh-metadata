# Groundwater2030: Data structure for field survey files

- Overview: The data are provided as four separate CSV tables that can be joined using common identifier fields unique to each groundwater source from the fieldwork. Sanitary risk and water quality datasets use their identifier fields as primary keys; the well customer dataset uses Well IDs as a foreign key.

- Files and primary keys:
  - Groundwater2030_sanrisk.csv — Description: Sanitary risk inspection of groundwater sources; Well ID field = Wellcode.
  - Groundwater2030_waterquality.csv — Description: Water quality test results; Well ID field = Wellcode.
  - Groundwater2030_well_owner_survey.csv — Description: Questionnaire survey of well owners; Well ID field = Well number.
  - Groundwater2030_WellCustomerSurvey.csv — Description: Questionnaire survey of well customers; Well ID field = Well number.

- Identifier scheme and relationships:
  - Unique identifiers within wellcode/well number take the form W1…n (well), S1…n (spring), B1…n (borehole). The prefix indicates source type.
  - An additional code O indicates wells in the baseline survey without current water quality data.
  - The owner and customer questionnaires may not be linkable to an individual well and are labeled None1, None2, etc., but still include neighbourhood information.

- Important data integration notes:
  - There may be multiple customers for a single groundwater source.
  - Joins across the four tables are performed via the identifier fields (Wellcode/Well number) to create a unified view of sanitary risk, water quality, well ownership, and customer perspectives.
  - Baseline-only wells (O) will lack corresponding water quality records.
  - Ensure data quality when merging PKs and FKs across datasets; account for potential one-to-many relationships with customers.
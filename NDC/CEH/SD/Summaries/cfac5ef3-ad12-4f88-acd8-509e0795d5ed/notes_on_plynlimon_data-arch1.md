# Plynlimon hydrochemistry data description

## Sampling regime
- Data cover March 2019 to March 2023.
- Sampling occurred every four weeks.
- See Plynlimon_site_information.csv for more details.

## Collection methods
- Refer to Plynlimon_field_measurements_and_methods.csv for collection methods.

## Sample Sites
- Refer to Plynlimon_site_information.csv for site details.

## Laboratory Instrumentation
- Refer to Description_of_column_headings.csv for instrumentation details.

## Nature and Units of Recorded Values
- Refer to Description_of_column_headings.csv for the nature and units of recorded values.

## Analytical Methods
- Refer to Description_of_column_headings.csv for analytical methods.

## Details of data structure
- Refer to Description_of_column_headings.csv for data structure details.

## Notes on reported values
- For hydrochemical values below the limit of detection (LOD), reported value is halfway between 0 and the LOD.
- Some chemicals have changing LODs over time, resulting in multiple rows per chemical per subperiod.
- Full determinant and method descriptions are provided in Description_of_column_headings.csv using the CAST thesaurus: https://vocabs.ceh.ac.uk/cast/en/

## Quality control and calibration
- pH, conductivity, and alkalinity measured at CEH Bangor laboratories.
- CEH Bangor participates in the LGC AquaCheck Proficiency Testing QA scheme.
- Other chemical analyses conducted at CEH Lancaster; UKAS-accredited to ISO 17025:2005 for many analyses.
- Data checked for missing values (blanks due to sampling, instrument failure, fieldworker error; periods with restricted access (e.g., Covid-19 in 2020) may reduce sampling).

## Data cleaning
- Fixed inconsistent quoting of SO4-S (SO4 vs SO4-S).
- Removed obvious gross errors in several variables, notably Cl.
- Fixed inconsistent bromide units (mg/L vs μg/L).
- Corrected pH data issue for the Afon Cyff/Gwy, where values were swapped since August 2022.

## Other information useful to interpretation
- Rainfall volume for Carregwen rain (C) chemistry is recorded from a rain gauge near the Hafren (B) site, not the Carregwen Standard gauge AJ.
# Sampling regime

- Timeframe and frequency
  - Sampling was weekly from June 2011 to December 2011.
  - Sampling shifted to fortnightly from January 2012 onward.

- Sample locations and change during a leaf litter experiment (2013)
  - Primary sites: Lower Hore (A), Lower Hafren (B), Cyff (AE), and Gwy (AF).
  - From 15/01/2013 to 24/09/2013, samples were taken roughly 100 to 150 meters upstream of the normal sample point due to a leaf litter addition experiment.
  - Coordinates for the upstream sampling during this period:
    - Lower Hore: Easting 284337, Northing 287238
    - Lower Hafren: Easting 284228, Northing 287936
    - Gwy: Easting 282281, Northing 285399
    - Cyff: Easting 282094, Northing 284246

- Handling of reported values and detection limits
  - Values below the limit of detection (LOD) are treated differently across periods:
    - 18/10/2011–27/03/2012: reported as measured by the instrument (no imputation described).
    - 17/04/2012–08/03/2016: reported as a value halfway between 0 and the LOD.
  - LOD details and the exact methods are described in Description_of_column_headings.csv using the CAST vocabulary.

- Rainfall data note
  - A value of 9999 in the Rainfall (mm) column indicates that the rain gauge was overflowing.

- Data provenance, methods, and documentation
  - Full determinant methods and column descriptions are provided in Description_of_column_headings.csv (CEH Analytical Services Thesaurus link available).
  - See Plynlimon_site_information.csv for additional site details and sampling context.

- Quality control and laboratory standards
  - pH, conductivity, and alkalinity measured at CEH Bangor laboratories; participate in the LGC AquaCheck Proficiency Testing scheme to ensure quality and comparability.
  - All other chemical analyses performed at CEH’s Centralised Analytical Chemistry Group (Lancaster); UKAS-accredited to ISO 17025:2005 for many analyses.

- Data completeness and caveats
  - Data have been checked for missing values; blanks indicate missing data.
  - Missing data may result from insufficient sample (e.g., rainfall), instrument failure, halted analyses (e.g., metals analysis stopped on 12/03/2013), or fieldworker error.

- Data usage considerations for analysis
  - The dataset combines hydrochemical measurements with rainfall data and notes the upstream sampling during a leaf litter experiment, which may affect hydrological and chemical measurements.
  - When integrating datasets, account for period-specific handling of below-LOD values and the potential spatial shift in sampling location during 2013.
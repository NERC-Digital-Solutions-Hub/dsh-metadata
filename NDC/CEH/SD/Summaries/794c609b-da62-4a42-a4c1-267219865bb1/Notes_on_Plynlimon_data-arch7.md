# Sampling regime

- Overview of sampling frequency and periods:
  - Weekly sampling from June 2011 to December 2011.
  - Fortnightly sampling from January 2012 onward.
  - 15/01/2013 to 24/09/2013: additional samples for four sites taken ~100–150 meters upstream of normal sample points due to a leaf litter addition experiment (15/01/2013–18/01/2013).

- Sample locations and coordinates:
  - Lower Hore (A): Easting 284337, Northing 287238.
  - Lower Hafren (B): Easting 284228, Northing 287936.
  - Cyff (AE): Easting 282094, Northing 284246.
  - Gwy (AF): Easting 282281, Northing 285399.
  - Note: For the leaf litter experiment period, samples were collected upstream of the regular points at the listed coordinates.

- Data handling and reporting notes:
  - Values below the detection limit (LOD) are reported differently over time:
    - 18/10/2011–27/03/2012: reported as produced by the analysis instrument.
    - 17/04/2012–08/03/2016: reported as a value halfway between 0 and the LOD.
  - LOD values are described in Description_of_column_headings.csv.
  - Rainfall values: 9999 indicates rainfall gauge overflow.

- Data structure and references:
  - Full determinant descriptions and methods are provided in Description_of_column_headings.csv ( utilisez CAST: CEH Analytical Services Thesaurus).
  - Sampling regime details linked to Plynlimon_site_information.csv.

- Quality control and provenance:
  - pH, conductivity, and alkalinity measured at CEH Bangor laboratories; these labs participate in the LGC AquaCheck proficiency testing.
  - Other chemical analyses conducted at CEH’s Centralised Analytical Chemistry Group (CEH Lancaster); UKAS-accredited to ISO 17025:2005 for many analyses.
  - Data checked for missing values; blank cells indicate missing data due to e.g. insufficient samples, instrument failure, halted analyses, or fieldwork errors.

- GIS and data use considerations:
  - Data span multiple sites and time periods, with a notable shift in sampling location for 2013.
  - Coordinate references provided for spatial mapping; verify the coordinate system (likely UK national grid) when integrating with GIS projects.
  - Awareness of LOD handling and potential gaps is essential for accurate spatial-temporal analyses.
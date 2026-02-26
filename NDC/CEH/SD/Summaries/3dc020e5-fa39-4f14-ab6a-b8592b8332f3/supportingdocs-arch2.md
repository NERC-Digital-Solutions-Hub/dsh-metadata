# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

## Overview
- Biological data: invertebrate abundances (macroinvertebrates) in peatland ponds.
- Physical data: location, altitude, pond morphology (dimensions, volume, etc.), and related site characteristics.
- Chemical data: dissolved ions, nutrients, and water quality indicators (e.g., pH, dissolved oxygen, temperature, DOC, metals).
- Purpose: support analysis of how invertebrate communities colonise and establish in restored peatland ponds over time, quantify changes in abundance and diversity (alpha and beta), and identify associations between physico-chemical variables and ecological communities.

## What was recorded and data formats
- Biological data: invertebrate abundances (identified to species where possible).
- Physical data: geographical coordinates, altitude, aspect, pond dimensions (long/short axis, perimeter), volume, and related attributes; pond age and restoration year.
- Chemical data: dissolved oxygen, water temperature, pH on site; lab-measured total nitrogen (TN), total phosphorus (TP), dissolved organic carbon (DOC), aluminum (Al), iron (Fe), silica (Si); additional ions/solutes as listed.
- Data files (four CSVs):
  - Chron_nat_inverts.csv (82 columns): invertebrate taxa abundances across chronosequence ponds; pond codes indicate site and pond number; includes naturally-formed ponds.
  - MH_inverts.csv (45 columns): invertebrate taxa abundances for chronosequence ponds (multi-pond per site).
  - Chron_natural_physical_chemical.csv (26 columns): pond metadata, location, sampling date, pond age, coordinates, elevation, dimensions, volume, temperature, DO, pH, and solutes.
  - MH_physical_chemical.csv (26 columns): detailed pond physico-chemical data per pool with explicit field mappings, units, and measurement methods.

## Study area and sampling design
- Location: peatland ponds in the Pennine hills, northern England.
- Ponds: 105 total sampled across multiple sites; six main peatlands used for chronosequence analyses, plus naturally-formed ponds.
- Sites listed (examples): Moor House, Tennant Gill, Cold Fell, Yad Moss, Halton Lea, Oughtershaw Beck; several ponds are natural (denoted with n).
- Sampling regime:
  - Chronosequence design with repeated sampling across years (2013–2014) and multiple ponds per site.
  - Regular sampling every two months from 04/2013 to 06/2014 (ages 4–18 months); one interruption due to snow.
  - On each visit, five ditches were sampled and one pond per ditch was selected randomly; ponds disturbed for sampling due to small size; independent ponds sampled each visit.
  - 20 naturally-formed ponds studied in 07/2012; sampling locations chosen with landowner access in mind.
- Objectives: examine colonisation dynamics, changes in abundance and diversity, and linkages between physico-chemical conditions and aquatic communities.

## Field and laboratory methods
- Biological sampling:
  - Macroinvertebrates collected with a long-handled net (250-µm mesh) using 2 minutes across mesohabitats (open water, floating vegetation, littoral vegetation, bottom sediments) plus 1 minute searching for surface-dwelling taxa.
  - Specimens preserved in 70% methylated spirits and transported to lab.
  - Sorting and identification to species level where possible; chironomids sometimes subsampled (n=50) for finer resolution.
  - Chironomids prepared via KOH digestion, acetic acid treatment, and mounting for microscopy.
- Physical measurements on site:
  - Altitude and location recorded with GPS; aspect derived from coordinates; pond dimensions measured (long axis, short axis, perimeter) with tape; depth measurements (minimum, maximum, mean) via multiple readings; water volume estimated from area and mean depth.
- Chemical measurements on site and in lab:
  - On-site: dissolved oxygen, water temperature, and pH measured with a portable HACH HQ30d meter (sensor in upper 10 cm).
  - pH sensor failed in month 12; missing values imputed using a statistical relationship with magnesium (r = 0.81) across other samples.
  - On-site water sample (50 mL) filtered for lab analyses of TN, TP, DOC, Al, Fe, Si using specified instruments (Analytikjena multi N/C 2100, San++ FC analyzer, iCAP7600 Duo ICP-OES).
- Quality checks:
  - Macroinvertebrate specimens verified by independent experts.
  - Calibration of DO, temp, pH sensors before each field visit.
  - Laboratory equipment calibrated with standards across and beyond sample ranges.

## Data structure and content
- Four CSV files with detailed column mappings (see above for file-specific descriptions).
- Pond identifiers are coded to align between fauna and physico-chemical data (e.g., MHC06 for Moor House Chronosequence pond 06; nWFN01 for a natural WiddyBank Fell pond).
- Units and methodology clearly annotated in the data dictionary embedded in the file descriptions (e.g., depth in cm, volume in m3, concentrations in mg/L or equivalents, dates in standard format).

## Quality assurance and completeness
- Completeness: dataset described as complete; five pH values missing due to sensor failure; imputed using established relationship with Mg concentrations.
- Data validation: independent verification of macroinvertebrate specimens; calibration of field sensors and laboratory instruments prior to analyses.
- Replicability: explicit sampling design, site details, and measurement methods provided to support reproducibility and long-term monitoring.

## Relevance for environmental monitoring and analysis
- Provides a standardised, multi-faceted dataset linking biotic communities to physical habitat features and water chemistry in peatland ponds.
- Enables monitoring of restoration effects (rewetting) on aquatic invertebrates and associated environmental conditions over time.
- Supports analysis of alpha and beta diversity changes and the identification of physico-chemical drivers of community structure.
- Designed for integration into monitoring platforms and portals, with datasets stored in accessible CSV formats and clear provenance.
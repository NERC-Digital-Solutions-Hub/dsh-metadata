# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

## Overview
- Dataset collates relative abundance of antimicrobial resistance genes from DNA in soils around Newcastle upon Tyne, alongside concentrations of PAHs and metals.
- Sample sites preselected by prior metal concentration studies and land-use; four treatment categories: low-metal/rural, low-metal/urban, high-metal/rural, high-metal/urban.
- Sampling conducted in June 2016 from the upper soil horizon (<15 cm); samples refrigerated until processing.

## Fieldwork and sampling design
- Location selection based on previous metal concentration data and land-use considerations.
- Four treatment groups representing combinations of metal level and urban/rural contexts.
- Depth restricted to the upper horizon (<15 cm).

## Analytical methods
- Soil moisture: measured in triplicate after drying at 105°C.
- Total Organic Carbon (TOC): determined in triplicate with a LECO CS244 analyzer; reported as % of dry weight.
- Total Kjeldahl Nitrogen (TKN): quantified using APHA 2010 standard methods.
- Soil pH: ISO 10390:2005 procedure; slurry prepared 1:5 in deionised water; measured with standard pH meter.
- PAH analyses: performed by Northumbrian Water Scientific Services using Soxhlet extraction followed by GC-MS.

## Nature of recorded units
- PAHs: parts-per-million (mg/kg or ppm) in soil.
- TOC and TKN: expressed as % of dry-weight.

## Data structure and schema
- Main columns:
  - Rural/Urban (A)
  - Location (B): common name
  - Latitude (C)
  - Longitude (D)
  - pH (E)
  - Total Organic Carbon (%) (F)
  - Total Kjeldahl (%) (G)
  - EPA 16 Priority PAH compounds (H–W)
  - Total PAH (sum of EPA16) (last column)
- EPA 16 PAH list includes naphthalene, acenaphthylene, acenaphthene, fluorene, phenanthrene, anthracene, fluoranthene, pyrene, benzo[a]anthracene, chrysene, benzo[b]fluoranthene, benzo[k]fluoranthene, benzo[a]pyrene, indeno[1,2,3-cd]pyrene, dibenzo[a,h]anthracene, benzo[g,h,i]perylene.
- Units are aligned with the recorded measurements above.

## Provenance, standards, and references
- Standards referenced: APHA (2010) Standard Methods for the Examination of Water and Wastewater; ISO 10390:2005 (Soil Quality – Determination of pH).
- Methodological context: Rothwell & Cooke (2015) related to background concentration calculations for urban soils.

## Data quality and governance considerations
- Quality assurance cues:
  - Triplicate measurements for moisture, TOC, and TKN indicate internal QA capability.
  - Use of recognized standard methods and instruments for measurements.
- Potential limitations to document and manage:
  - Geographic scope limited to NE England soils around Newcastle; may affect generalizability.
  - Depth limited to upper horizon; excludes deeper soil layers.
  - Site selection based on prior data; may introduce selection bias.
  - Metadata completeness essential for discoverability (date, exact coordinates, sampling protocol, lot identifiers, instrument calibrations).

## Accessibility, sharing, and updates
- Dataset structure implies portal/catalogue readiness, with explicit data fields to facilitate discoverability.
- Procedures for updates or changes to methods, sample reprocessing, or new measurements are not specified and should be defined to ensure timely, reliable updates and versioning.
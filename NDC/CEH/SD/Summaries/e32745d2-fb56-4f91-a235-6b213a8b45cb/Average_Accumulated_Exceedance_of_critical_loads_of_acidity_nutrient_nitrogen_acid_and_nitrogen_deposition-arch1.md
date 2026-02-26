# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2013-15

## Overview
- Purpose: Quantify exceedances of habitat-specific critical loads due to acid and nitrogen deposition across UK 1x1 km grid squares for 2013–2015.
- Core concept: AAE aggregates exceedances across habitats within each grid cell, normalised by total habitat area in that cell.

## How AAE is calculated
- AE for a habitat: AE = exceedance (keq ha-1 year-1) × habitat area exceeded (ha).
- AAE for a grid square: AAE = total AE across habitats in the square / total habitat area in the square (keq ha-1 year-1).
- Conversion notes: For nutrient nitrogen, 1 keq ha-1 year-1 = 14 kg N ha-1 year-1. AAE values below the critical load are set to zero. Acidity AAE cannot be split into S or N.

## Habitats included
- Acidity (AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and both productive and unmanaged woodland types (coniferous and broadleaved).
- Nutrient nitrogen (AAE): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, various productive and unmanaged woodlands, beech and oak woodland, Scots pine woodland, other unmanaged woodland, dune grassland, and saltmarsh.

## Data coverage and sources
- Geographic scope: UK 1x1 km grid squares, with some differences in coverage between acidity and nitrogen datasets.
- Data provenance: UK Methods Report (Hall et al., 2015) for calculation of critical loads and exceedances; Trends Report 2017; CBED deposition data via EIDC.
- Metadata/uncertainty resources: Hall et al. (2015) methods; meta-data for Critical Loads data; UK Biodiversity Indicator on pollution (B5a).

## Data structure and files
- Two data files:
  - acidhab_AAE_2013-15.csv (AAE for acidity)
  - nutnhab_AAE_2013-15.csv (AAE for nutrient nitrogen)
- Common fields in both:
  - East_m, North_m: centre coordinates in OSGB (metres)
  - Unique1km: unique 1x1 km grid-square identifier
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- Data structure note: AAI values linked across acidity and nitrogen via Unique1km where both datasets have data.

## Use, interpretation, and cautions
- Interpretation of exceedances: Exceedance indicates potential long-term harm under steady-state assumptions; current exceedance does not imply immediate damage.
- Habitat maps vs. other maps: The habitat distribution maps used for critical loads/exceedances may differ from other UK habitat maps, affecting total mapped habitat areas.
- Recovery dynamics: Reducing deposition below the critical load may not yield immediate ecological or chemical recovery; recovery can be slow with long time lags.
- Coverage caveats: The datasets include only areas with data suitable for critical load calculations; some areas are not represented due to data availability.

## Quality, uncertainty, and documentation
- Quality framework: Methods aligned with UNECE CLRTAP; transparency via Hall et al. (2015) Methods and related documentation.
- Uncertainty notes: Uncertainties in habitat mapping and critical loads are acknowledged; refer to Hall et al. (2015) and the Critical Loads metadata for details.
- Related references: Hall, Smith, Dore (2017) Trends Report; Hall, Curtis, Dore, Smith (2015) Methods report.

## Additional information and access
- Data are linked to broader UK critical loads and CBED deposition datasets; further information available from EIDC and CEH metadata portals.
- Related outputs: Trends Report 2017; UK Biodiversity Indicator on pollution (B5a).
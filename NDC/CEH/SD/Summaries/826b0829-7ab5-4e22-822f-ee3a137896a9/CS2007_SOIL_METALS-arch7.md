# Soil metals 2007 [Countryside Survey], Great Britain

## Overview
- Countryside Survey 2007 soil metals dataset for Great Britain.
- Analysed from 402 soil cores drawn from up to 256 1 km squares surveyed in 2007.
- Data collection involved ICP-OES and (from 2007) ICP-MS to expand analyte suite.

## Data scope and structure
- Sample design: soil cores from 1 km squares, with plots within each square.
- Analytes: up to 27 elements; key metals include Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg, among others.
- File details: CS2007_SOIL_METALS.csv documents metals concentrations (ppm) alongside location and classification data.
- Columns of interest:
  - SQUARE (1 km square code)
  - PLOT (plot ID within square)
  - YEAR (survey year)
  - Cd (CD), Cr (CR), Cu (CU), Ni (NI), Pb (PB), Zn (ZN), Al (AL), Ti (TI), Mn (MN), As (AS), Se (SE), Mo (MO), Hg (HG)
  - LC07 (ITE Land Class 2007) and LC07_NUM (numeric code)
  - COUNTRY (ENG, SCO, WAL)
  - COUNTY07 (county or council)
  - EZ_DESC_07 (Env. Zone description)

## Spatial context and resolution
- Spatial unit: 1 km x 1 km squares across Great Britain.
- Per-square and per-plot detail enables map-based visualization of metal distributions and landscape context.
- Land classification and environmental zone metadata accompany metal measurements for enriched GIS analysis.

## Data quality and methods
- Laboratory methods:
  - Digestion by Aqua Regia (The Standing Committee of Analysts method).
  - Analyses by ICP-OES; ICP-MS added in 2007 to broaden detectable analytes.
  - Current CEH Lancaster standard suite up to 27 analytes.
- Quality assurance and control:
  - ISO 17025 accredited laboratory (UKAS).
  - Quality Control target: total analytical error of 20% (10% precision, 10% bias).
  - QC: action limits and warning limits; data from batches outside limits may be rejected.
  - CRM checks and re-analysis if issues detected; after 100 samples, targets may be reviewed; potential re-instatement of previously rejected data.
- Documentation and standards:
  - Protocols and QA details documented in Countryside Survey Soils Manual (Emmett et al. 2008) and CS 2007 technical reports.
  - Cross-checks performed when methods changed; results and procedures aligned with established CS methodologies.

## Sampling strategy and temporal scope
- Stratified sampling based on Land Classes to capture environmental gradients; GB-wide representativeness for England, Scotland, and Wales.
- 2007 survey used 591 sample squares; prior surveys used different corner locations (soil cores collected 0–15 cm depth; later surveys varied sampling corners).
- Years covered: 2007 (primary dataset); related publications span 2008–2010 CS Soils reports and UK results.

## Data usage and acknowledgments
- All CS data usage must acknowledge: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Acknowledgement and copyright noted on copies, publications, and presentations.
- References and documentation include CS Soils Manual and CS technical reports; links to CS data and publications are provided in the dataset documentation.

## Provenance and references
- Core references: Emmett et al. 2008 Countryside Survey: Soils Manual; Emmett et al. 2010 Countryside Survey: UK Results from 2007.
- Land classification context: ITE Land Classification of Great Britain (Bunce et al. 1996, 1981; 2007 dataset).
- Analytical and chemical analysis references: Allen (Chemical Analysis of Ecological Materials, 2nd ed.), and related CS technical reports.
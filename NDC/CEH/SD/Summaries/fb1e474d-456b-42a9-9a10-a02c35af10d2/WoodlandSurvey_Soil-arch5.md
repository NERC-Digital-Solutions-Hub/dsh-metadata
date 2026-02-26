# Woodlands Survey soil data 1971-2001

## Overview
- Datasets from a long-term survey of 103 broadleaved woodlands in Britain (1971 baseline; re-surveys in 2000, 2002/2003 labeled as 2001).
- Ecological data collected at site level and within 16 randomly placed 200 m2 plots per site.
- Variables include plant community (canopy and ground flora), soil pH, soil organic matter (SOM), habitat management, and other plot/site descriptors.
- Data are accompanied by analyses linking ecological change to drivers (atmospheric deposition, climate, canopy change, management).
- Key publications provide methodological and analytical context; users should consult Kirby et al. (2005), Corney et al. (2004), etc.

## Survey design and methods
- Stratified sampling across the study area.
- Field methods follow Bunce & Shaw (1973) standardized survey methods; a field handbook is included in supporting documentation.
- Re-surveys conducted using identical methods to enable comparison over time.

## Related datasets
- Countryside Survey (www.countrysidesurvey.org.uk)
- Steele (1968). National survey of woodlands (relevant context)
  
## Originator details
- 1971: R.G.H. Bunce & M.W. Shaw (Woodland Ecology Section, Nature Conservancy - Merlewood)
- 2001-2003: Simon Smart, Helaina Black (CEH Lancaster); Keith Kirby (English Nature); Phil Corney (University of Liverpool)

## Data structure and contents
- Site and plot identifiers:
  - Site: numeric code (1–103)
  - Plot: numeric (1–16)
- Soil and site measurements (examples):
  - pH1971: soil pH in 1971
  - pH2003: soil pH in the 2000s
  - pH1971_QA_repeats: repeat pH measurements from 2000 on archived 1971 samples
  - SOM1971: soil organic matter in 1971 (%)
  - SOM2003: SOM in the 2000s
  - SOM1971_QArepeats: repeat SOM measurements from 2000 (%)
  - MSG: Major Soil Group code (Avery 1973)
  - SG: Soil Group code (Avery 1973)
  - SSG: Soil Sub-group code (Avery 1973)
  - Major_Soil_Group: description of Major Soil Group
  - Soil_Group: description of Soil Group
  - Soil_subgroup: description of Soil Sub-group
- Data formats:
  - Numeric for sites/plots and most measurements
  - Text for descriptive soil groupings
- Metadata indicates field methods, QA practices, and the exact coding schemes used for soil classification.

## Data provenance and lineage
- Data collected 1971 and re-surveyed in 2000–2003 using the same field methods.
- Ground-truthing and QA repeats exist for select measurements.
- Linkages to external explanatory data (atmospheric deposition, climate, canopy change, management) used in subsequent analyses.
- Publications cited provide methodological and analytical context for data interpretation.

## Access, usage, and governance notes
- Documentation notes that users should consult associated publications for deeper methodological and analytical details.
- Data are designed for long-term ecological change analyses, with standardized formats to support cross-site comparisons.
- Clear provenance and originator details support data trust, reproducibility, and proper attribution.

## Quality assurance and updates
- Repeated measurements (QA repeats) implemented for key soil metrics.
- 2001–2003 resurvey maintained methodological consistency with 1971 baseline to enable robust change detection.
- Metadata includes detailed variable descriptions and coding schemes to support interoperability and discoverability.

## References
- Avery, B. W. 1973. Soil Classification in the Soil Survey of England and Wales.
- Corney, P.M. et al. 2004. The effect of landscape-scale environmental drivers on vegetation in British woodlands.
- Haines-Young, R.H. et al. 2003. Changing landscapes, habitats and vegetation diversity across Great Britain.
- Kirby, K.J. et al. 2005. Measuring Long Term Ecological Change in British woodlands (1971-2001). English Nature Research Reports 653.
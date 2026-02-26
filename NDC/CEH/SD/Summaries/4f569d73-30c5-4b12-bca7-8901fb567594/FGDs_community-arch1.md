# Supporting documentation for the dataset Qualitative data on land use change and ecosystem services from participatory study in northeastern, Kenya (August - October, 2013)

## Overview and aims
- Qualitative dataset documenting land use change, ecosystem services, livelihoods, wealth, livestock, and human disease perceptions.
- Cross-sectional study with village as unit; compares irrigated (Bura, Hola) and pastoral/riverine areas (Ijara, Sangailu).
- Aimed at capturing community perspectives and generating data for analysis of land-use dynamics and ecosystem service changes.

## Study design and sampling
- Sites: Ijara and Sangailu (pastoral), Bura and Hola (irrigated).
- Village selection: convenient sampling within irrigated sites; villages with farming as main livelihood identified (13 irrigated villages total) and 25 pastoral/riverine villages.
- Within villages: Focus group discussions (FGDs) with adults who have resided for ≥20 years.
- Sample structure: FGDs per village, typically 10–12 participants; in pastoral areas, gender-separated sessions (often two FGDs per village).

## Data collection methods
- Ethics: written or thumbprint consent obtained; information read to participants; sessions recorded with permission.
- Team composition: moderator, translator, note-taker.
- Instruments: pretested FGD guide; visual tools and exercises.
- Data collection activities: 
  - Simple ranking, proportional piling, disease incidence scoring, community resource mapping, seasonal calendars.
  - Wealth categorization based on livestock, education, housing, assets, energy, livelihood sources, and access to services; wealth categories defined by participants (poor, middle, rich).
- Data quality aids: notes validated against transcripts; informal discussions with key informants used to clarify ambiguous data.

## Data processing and analysis
- Transcription: FGDs transcribed; identifiers removed; transcripts saved as text for analysis.
- Data processing: Word (2013) transcripts converted to text; prepared for text mining.
- Analytical framework: Hennink et al. (2011) qualitative methods; three researchers coded transcripts against predetermined themes.
- Reliability: inter-coder agreement checks conducted; themes compared within and across sites to identify patterns and linkages.
- Data management: transcripts organized by site, village, and group; exercise-derived data flagged where used.

## Quality control and validation
- Multidisciplinary team enabled multidimensional probing.
- Validation of notes against digital transcripts increased accuracy.
- Ambiguities clarified through discussions with local key informants.

## Data files and structure
- Dataset 1: 39 text transcripts (FGD records), named by site, village, and group.
- Dataset 2: DDDAC_kenya_fgdscores.csv containing proportional piling outputs and contextual variables.
  - Key variables include:
    - Serial_no, date, site (Bura, Hola, Sangailu, Ijara), village, group (gender).
    - Rich_a, Middle income_a, Poor_a (proportions of households by wealth category).
    - goats_a, sheep_a, donkeys_a, poultry_a, camels_a (proportions of livestock types).
    - site (irrigated, pastoral, or riverine).
  - Note: “a” denotes proportions from proportional piling; missing values where the exercise was not conducted.

## Data provenance and personnel
- Principal contributors: Salome Bukachi (design, implementation, data analysis), Caroline Mwihaki (implementation and analysis), Grace Delia (design), Bernard Bett (design, implementation, data analysis).

## Geographical scope
- Spatial extent defined by coordinates: longitude 38.93 to 41.14, latitude -1.89 to -0.64.

## References and methodological framework
- Qualitative data analysis guided by Hennink, Hutter, Bailey (2011) Qualitative Research Methods.

## Limitations and considerations for analysts
- Use of convenience sampling within sites; not all villages across zones may be represented.
- Proportional piling used in some FGDs; not uniformly applied across all sessions.
- Qualitative data reflect perceptions and self-reported indicators; cross-site comparability may require careful normalization.
- Data pertains to a historical period (Aug–Oct 2013) and may require contextual updating for current analyses.
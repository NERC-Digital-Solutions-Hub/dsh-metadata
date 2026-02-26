# Metadata for 'Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020'

## Overview
- Long-term field trial of Pinus sylvestris across three field sites in Scotland to collect field phenotypes from 2013 to 2020.
- Seed origin: seeds from ten trees from each of 21 native Scottish populations; collected in March 2007 and germinated in June 2007; populations chosen to represent the native range with three populations per seed zone.
- Data repository entry: field phenotypes are captured in a single data file titled FieldTraits.txt.

## Experimental Design and Sampling
- Seed handling: dormancy break by soaking seeds, storage in cool conditions, and transplantation to controlled nursery conditions.
- Nurseries: three nurseries (NW, NG, NE) prior to field planting, with varied origins for cohorts.
- Field trial setup (2012 planting): three sites in Scotland
  - FS: Yair (south, field site), coordinates 55.603625, -2.893025
  - FE: Glensaugh (east), coordinates 56.893567, -2.535736
  - FW: Inverewe (west), coordinates 57.775714, -5.597181
- Randomised blocks and spacing: 3 m x 3 m spacing; four blocks at FS and FE, three blocks at FW; each block contains one tree from each of eight of the ten families per population (168 trees per block); guard row around blocks.
- Plant material: one tree per block chosen from eight of the ten families per population; N varies per site; some replacements occurred at FS where certain populations were underrepresented.
- Population/family structure: families are defined as offspring from the same mother tree; notation and tracking via PopulationCode, Family, FieldCode, Block, Row, and Column.

## Data Collected and Variables
- Measurements and timeframe
  - Height: HA13–HA20 (mm) at FE and FW (2013–2020); HA14–HA20 and earlier years for FS (2014–2020 for FS).
  - Height increments: HI13–HI20 (mm) corresponding to yearly height increases.
  - Base stem diameter: DA13–DA20 (mm) at FE and FW (2013–2020); DA20 measured at FS in 2020.
  - Diameter increments: DI13–DI20 (mm) corresponding to yearly diameter changes.
  - Budburst phenology: BD15–BD19 (days) for 2015–2019; BD15_4, BD15_5, BD15_6, etc., for year-by-year stages (days to reach budburst stages 4–6) across multiple years.
  - Stage timing: BT15_4, BT15_5, BT15_6, BT16_4, BT16_5, BT16_6, BT17_4, BT17_5, BT17_6, BT18_4, BT18_5, BT18_6, BT19_4, BT19_5, BT19_6 (days since 31 March of the respective year to reach budburst stages 4–6).
- Data file and schema
  - File: FieldTraits.txt
  - Key columns: PopulationCode, Description; Family, Description; FieldSite (FE, FS, FW) with FieldSite names corresponding to Glensaugh (FE), Yair (FS), Inverewe (FW); FieldCode (unique tree code; ranges 5001–5672, 6001–6004, 7001–7672); Block; Row; Column; HAxx, HIxx; DAxx, DIxx; BDxx; BTxx.
  - Units: Height/diameter in millimeters (mm); Days to budburst or to stages in days.
  - Population and family coding: PopulationCode links to population; Family groups are individuals from the same mother tree.

## Data Structure, Schema, and Metadata Details
- The dataset comprises a single file FieldTraits.txt with all measurements and identifiers.
- FieldCode ranges indicate site-specific tree coding:
  - FW: 5001–5672, 6001–6004, 7001–7672
- Site coding:
  - FE: Glensaugh (east)
  - FS: Yair (south)
  - FW: Inverewe (west)
- Data relationships:
  - PopulationCode maps to population description.
  - Family maps to individuals sharing a mother tree.
  - Block/Row/Column define spatial placement within each site.
- Temporal coverage:
  - Height/diameter data spanning 2013–2020 (varying by site).
  - Phenology data spanning 2015–2019 (2020 not collected due to COVID-19).

## Data Quality, Provenance, and Limitations
- Provenance captured: seed collection in 2007, nursery propagation, and definitive field planting in 2012 with randomised block structure.
- Replacements: nine populations were replaced at FS due to insufficient trees, indicating incomplete representation at one site.
- Data gaps: phenology measurements not possible in 2020 due to COVID-19 restrictions.
- Cross-site consistency: multi-site design with standardized measurement protocols across FE and FW, and a slightly shorter measurement window for FS.

## Governance, Access, and Stewardship Considerations
- Metadata richness: coordinates for origin and field sites; explicit site naming; detailed field coding and measurement definitions.
- Data stewardship needs:
  - Maintain and version FieldTraits.txt with clear change logs.
  - Track replacements and any changes to population/family representation.
  - Ensure consistency of units and definitions across sites and over time.
  - Plan for future updates to fill data gaps (e.g., any post-2020 updates or corrections).

## Potential Uses and Relevance for Data Stewards
- Longitudinal analysis of growth (height and basal diameter) across environmental contexts (three field sites).
- Genotype-by-environment studies leveraging seed-zone representations and family structure.
- Phenology dynamics across years, with attention to year-specific budburst timing.
- Cross-site data discovery and integration with other Scots pine datasets for broader meta-analyses.
- Data sharing and governance: the FieldTraits.txt file provides a well-structured schema suitable for cataloguing and reuse, with clear provenance and site-specific metadata.
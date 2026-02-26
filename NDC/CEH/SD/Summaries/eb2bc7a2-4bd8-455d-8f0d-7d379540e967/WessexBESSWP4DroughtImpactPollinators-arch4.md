# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation

## Overview
- A dataset from a field experiment examining how plant functional diversity and experimentally induced drought affect floral resources and pollinator visitation.
- Collected on the Winklebury Hill experiment site (Wiltshire, UK) during 2015–2016.
- Focuses on floral resources (flower abundance, diversity, nectar quantity/quality) and pollinator visitation across different plant functional groups and drought treatments.

## Datasets included
- NERCPropNectar.csv: Nectar presence and counts per raceme; treatment information and sampling details.
- NERCNectar.csv: Nectar measurements per flower (volume, sugar concentration) and derived nectar quantity; concentration data may have missing values.
- NERCFloralSurveys.csv: Floral surveys by subplot; species-level flowering counts; pollinator visit data (two survey rounds).
- NERCPollinatorSurveys.csv: Pollinator visit data by subplot and survey; taxonomic/pollinator details and visit counts.

Linking keys to combine datasets:
- PlotID, SubplotID, RacemeID, SurveyID are consistent across files.
- PlotID can link to Fry et al. 2017/2018 datasets for extended context.

## Experimental design and data collection
- Site: Ex-arable calcareous grassland, 8 m x 8 m plots with 2 m gaps; 24 plots total arranged in a grid with random allocation of treatments.
- Plant functional groups (FG) and diversity:
  - FG1, FG2, FG3 with varying root traits and leaf characteristics.
  - All combinations of FG1/FG2/FG3 implemented (7 across, 6 down grid), replicated across six rows.
- Treatments:
  - Drought (D): rain exclusion with shelters for six weeks to simulate a once-in-100-years drought.
  - Control (C): ambient rainfall.
  - Roofed control (R): roof with holes to control for roof-related effects (temperature/light).
- Drought timing: shelters deployed from early June to mid-July in 2015 and 2016.
- Nectar measurements:
  - Focal species chosen for nectar sampling; racemes bagged for 24 h to prevent visitation.
  - Nectar volume measured with microcapillary tubes; nectar sugar concentration measured with a refractometer; calculations to estimate sugar produced per flower.
- Floral resource surveys:
  - 1 m^2 quadrats within subplots; identification to species; counting floral units (groups of flowers that can be visited without moving).
  - Pollinator visits recorded over 10-minute intervals; observer noted visitor identity (morphotype) and plant species visited.
  - Two rounds of surveys conducted in July, with randomized plot order.
- Data quality and ethics:
  - Field protocols followed; data entered in MS Access; missing data noted in metadata.
  - Ethics approval by CLES Penryn Research Ethics Committee (University of Exeter).
  - Data linked to broader Winklebury Hill ecosystem datasets (Fry et al. 2017, 2018).

## Key variables and data quality
- Nectar data: includes nectar volume, concentration, total nectar per flower; some concentration values missing (noted as missing 144/703 in Concentration_Absolute).
- Floral surveys: counts of floral units by species; FG composition and diversity; date of survey.
- Pollinator surveys: number of visits per plant species; pollinator codes and species classifications; two survey rounds.
- Metadata granularity:
  - Detailed field descriptions, units, and data types are provided for each file.
  - Some observer-related data gaps (e.g., 14.C subplot in first pollinator round missing due to error).
- Data linking and consistency:
  - Clear linking fields across datasets to enable joint analyses (PlotID, SubplotID, RacemeID, SurveyID).
- Limitations and caveats:
  - Missing concentration data in nectar measurements.
  - Occasional zero-visit records or missing subplot data due to observer error.
  - Complex, multi-year drought treatment adds temporal dimension to analyses.

## Data governance, provenance, and access
- Data collection approved by university ethics committee; project affiliated with NERC Environmental Information Data Centre.
- Datasets reference established literature and prior Fry et al. work for context.
- Documentation includes extensive metadata, protocol descriptions, and data processing notes to ensure reproducibility.

## Implications for data strategy and use
- Data discoverability and reuse:
  - Rich, well-documented metadata enables cross-dataset joins and integration with broader ecosystem datasets.
  - Consistent identifiers across files support end-to-end data lineage and traceability.
- Data quality management:
  - Identified gaps (e.g., concentration data missingness) highlight areas for improving data capture and standardization in future rounds.
  - Clear notes on data limitations (observer errors, drought timing) aid in robust analysis and bias assessment.
- User needs and applicability:
  - Useful for researchers evaluating how plant trait diversity and drought influence nectar resources and pollinator visitation.
  - Can be integrated with related Winklebury Hill datasets to model ecosystem functions like carbon and nutrient cycling in relation to plant functional diversity.
- Operational considerations:
  - MS Access as an initial data capture format suggests a need for transition to more scalable, query-friendly databases or data lakes for long-term data stewardship.
  - Ongoing documentation and data-quality flags should be maintained as new data are added or existing data are re-processed.
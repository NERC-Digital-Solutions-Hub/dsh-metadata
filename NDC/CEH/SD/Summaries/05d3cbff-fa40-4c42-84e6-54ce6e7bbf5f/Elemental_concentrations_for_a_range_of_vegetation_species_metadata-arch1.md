# Elemental meta-data

- The document defines a metadata schema for a centralised chemistry laboratory dataset containing elemental concentrations in plant species or soil samples.
- It records both sample-identifying information and a comprehensive set of elemental measurements, using multiple analytical methods.

## Overview of the dataset

- Purpose: to capture sample provenance, taxonomy, sampling context, and quantitative/semi-quantitative elemental concentrations.
- Primary identifiers: Laboratory_ID (CEH centralised chemistry laboratory unique sample identifier) and Sample_ID (CEH Radiochemistry laboratory unique sample identifier).
- Sampling context: Collection_Site and Sampling_date (dd/mm/yyyy).
- Biological/taxonomic context: Species (Latin name), Common_name, and taxonomic fields (Order, Family, Genus).
- Analytical scope: concentrations for a wide range of elements measured by ICPMS or ICPOES, with both quantitative and semi-quantitative entries, and with detection-limit (LOD) indicators.

## Key fields and data types

- Sample and site metadata:
  - Collection_Site: sampling location
  - Sampling_date: date of sampling
  - Species, Common_name: plant species info
  - Order, Family, Genus: taxonomic classification
- Element concentration data:
  - Numerous element-specific columns (e.g., Li_mg_kg_quantitative_mg_kg_dry; Be_<; Be_mg_kg_quantitative_mg_kg_dry; Na_ICPOES_mg_kg_quantitative_mg_kg_dry; Mg_ICPOES_mg_kg_quantitative_mg_kg_dry; many others across the periodic table)
  - Measurement types: quantitative (ICPMS or ICPOES) and semi-quantitative
  - Weight basis and units: mg/kg, typically dry weight; some entries indicate per kg dry weight or, in certain replicates, fresh weight
  - Replicates/variants: suffixes like 1, 2 to indicate multiple measurements or methods per element
- Data qualifiers:
  - "<" indicates concentration below the limit of detection (LOD)
  - n/a indicates data not available
  - Some columns specify “not applicable” for certain qualifiers

## Measurement methods and units

- Methods:
  - ICPMS (Inductively Coupled Plasma Mass Spectrometry) for many trace elements
  - ICPOES (Inductively Coupled Plasma Optical Emission Spectrometry) for others
- Quantitative vs semi-quantitative:
  - Many elements have quantitative measurements
  - Some elements or entries are semi-quantitative
- Units:
  - Concentrations reported primarily as mg per kg
  - Dry weight is the common basis; some entries reference fresh weight or specify the weight basis in the column name
- Format nuances:
  - Some columns include qualifiers for detection limits or data availability
  - Data may be split into multiple columns per element to accommodate different methods or replicates

## Data quality flags and missing data

- Below-LOD values are prefixed with "<" in the relevant columns.
- Data not available is indicated as n/a in the appropriate columns.
- The presence of multiple replicate/method columns per element implies careful handling needed for combining measurements.

## Structure and usage guidance for analysis

- The schema enables analyses linking sample provenance and taxonomy with multi-element chemical profiles.
- Facilitates cross-sample comparisons across species and sites, and predictive modelling of element accumulation.
- Analysts should:
  - Harmonise units and weight basis (dry vs fresh weight) across columns
  - Properly treat below-LOD values (consider censoring or imputation strategies)
  - Reconcile replicates/methods (1 vs 2 suffixes) when aggregating
  - Maintain clear provenance by tying element data to Laboratory_ID, Sample_ID, and Collection_Site
  - Leverage taxonomic metadata (Species, Order, Family, Genus) for phylogenetic or ecological analyses

## Practical implications for data-driven questions

- Enables correlation analysis between element concentrations and plant taxa, collection sites, or sampling dates.
- Supports development of predictive models for element uptake or accumulation across species or environmental contexts.
- Requires careful data cleaning to manage the extensive array of elements, measurement types, and potential missing or below-LOD values.
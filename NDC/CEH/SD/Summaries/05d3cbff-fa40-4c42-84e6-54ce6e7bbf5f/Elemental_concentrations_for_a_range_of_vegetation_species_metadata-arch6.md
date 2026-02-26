# Elemental meta-data

## Overview
- Metadata and data dictionary for a dataset of elemental analyses from CEH laboratories, linking sample identifiers, site, date, and taxonomic context to a large set of elemental concentration measurements.
- Captures both plant and soil samples, with laboratory- and site-level provenance to enable data integration and self-serve analytics.

## Core identifiers and sample context
- Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
- Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
- Collection_Site: Sampling site.
- Sampling_date: Date of sampling (dd/mm/yyyy).
- Species: Latin scientific name (n/a if soil sample).
- Common_name: Common name (n/a if not provided or soil sample).
- Order, Family, Genus: Taxonomic classification.

## Sample type and contextual data
- Indicates whether the record corresponds to a plant or soil sample.
- If soil sample, species-related fields may be n/a.
- These fields support ecological or policy-oriented analyses and public communication.

## Measurements and data structure
- A large panel of elemental concentration columns (e.g., Li, Be, Na, Mg, Al, Si, P, S, K, Ca, Ti, Cr, Mn, Fe, Co, Ni, Cu, Zn, Se, Rb, Sr, Y, Zr, Nb, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, W, Hg, Tl, Pb, Th, U).
- For each element, multiple measurement types may be present:
  - ICPMS or ICPOES methods.
  - Quantitative and semi-quantitative measurements.
- Data basis and units:
  - Primarily mg/kg (dry weight) or mg/kg (fresh weight) depending on element and column.
  - Some semi-quantitative columns specify weight basis (often dry weight); a few Nb columns are fresh weight.
- Detection status:
  - "<" indicates concentration below the limit of detection (LOD) in the corresponding column.
  - Some columns marked n/a or not applicable when data are not available or not relevant for the sample type.
- Data format notes:
  - A mix of directly quantitative values and semi-quantitative estimates across elements.
  - Some columns explicitly indicate data not available (n/a) or not applicable due to methodology or sample type.

## Units, detection flags and data quality
- Units include mg per kg (dry weight) and mg per kg (fresh weight) where stated.
- LOD handling through explicit "<" indicators in relevant columns.
- Presence of missing (n/a) or not applicable entries, reflecting incomplete data or inapplicable measurements for certain samples.

## Provenance and usage notes
- Data originates from CEH centralised chemistry laboratories with linking identifiers to facilitate traceability.
- Designed to enable data products such as dashboards, pivot tables, and self-serve analyses by combining sample metadata with elemental concentrations.
- Suitable for comparative analyses across species, sites, and elemental concentrations, with attention to methodological differences (ICPMS vs ICPOES) and the weight basis (dry vs fresh).

## Practical considerations for data use
- Align weight basis and units when comparing records (dry vs fresh weight).
- Handle below-LOD values appropriately (consider imputation or censoring strategies).
- Distinguish quantitative vs semi-quantitative columns when interpreting results.
- Use identifiers to join to higher-level metadata (site, date, taxonomy) for ecological or policy-oriented insights.
# Elemental meta-data

## Overview
- Metadata schema for CEH centralised chemistry laboratory data describing plant and soil samples.
- Combines sample identifiers, collection information, taxonomy, and multi-element concentration measurements.
- Captures method (ICPMS ICPOES), weight basis (dry or fresh), units (mg/kg), and data qualifiers (e.g., below detection limit).

## Key data model components

- Identifiers
  - Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
  - Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
- Collection data
  - Collection_Site: Sampling site.
  - Sampling_date: Date of sampling (dd/mm/yyyy).
- Taxonomy and naming
  - Species: Latin name of the plant species (n/a if soil sample).
  - Common_name: Common name (or n/a if not provided).
  - Order, Family, Genus: Taxonomic hierarchy (n/a if not applicable).
- Measurements and data structure
  - For each element, there are fields representing concentration values and qualifiers.
  - Methods indicated include ICPMS (mass spectrometry) and ICPOES (optical emission spectrometry).
  - Weight basis specified as dry weight (mg/kg_dry) or fresh weight (mg/kg_fresh) where applicable.
  - Units consistently expressed as mg per kg (mg/kg); some entries indicate “not applicable” or data not available.
  - Qualifiers for detection limits: columns with “<” denote concentrations below the limit of detection (LOD).
  - Semi-quantitative vs quantitative distinctions appear for many elements (e.g., Li_mg_kg_quantitative_mg_kg_d ry).
  - Replicate or paired columns indicated by suffixes such as 1 and 2 for several elements.
  - Numerous elements covered (e.g., Li, Be, Na, Mg, Al, Si, P, S, K, Ca, Ti, Cr, Mn, Fe, Co, Ni, Cu, Zn, Se, Rb, Sr, Y, Zr, Nb, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, W, Hg, Tl, Pb, Th, U, among others).

## Data quality and metadata indicators

- Detection limits
  - Numerous fields indicate below-LOD values with a “<” marker; some entries explicitly note “not applicable” where below-LOD values are not recorded.
- Measurement qualifiers
  - Distinction between semi-quantitative and quantitative measurements across different elements and methods.
- Data completeness
  - Some fields may be marked as n/a or not available; data completeness varies across elements and columns.
- Naming and unit consistency
  - Complex, with many element-specific columns and method- and weight-basis-specific variants; standardization is essential for cross-dataset comparability.

## Data governance and stewardship implications

- Standardization needs
  - Harmonize units and weight basis (dry vs fresh) and ensure consistent naming conventions for elements and methods.
- Handling below-LOD
  - Clearly define and consistently apply how < LOD values are stored and analyzed.
- Metadata completeness
  - Maintain comprehensive metadata (lab IDs, site, date, taxonomy) to enable discovery and interpretation.
- Data quality controls
  - Implement validation rules to ensure correct method assignment, weight basis, and presence/absence of replicates.

## Practical implications for Data Leaders

- Enables cross-study data integration by providing a detailed, method-specific metadata framework for elemental concentrations.
- Supports data discovery and reuse through explicit identifiers, site, date, taxonomy, and measurement details.
- Requires governance around unit normalization, LOD handling, and consistency of semi-quantitative vs quantitative data to ensure reliable analytics and reporting.

## Potential uses

- Comparative analyses of elemental profiles across plant species and collection sites.
- Environmental and policy-relevant assessments leveraging standardized metadata and concentration data.
- Data-driven prioritization of data collection gaps based on reported availability and completeness.
# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1

## Overview
- National estimates of Broad Habitat change (Habitats 1–17) between 1990, 1998, and 2007, calculated using the 2007 ITE Land Classification.
- Provides change in area by Land Class and Broad Habitat, with accompanying uncertainty.
- Mapping and methodological context referenced in foundational publications; data originate from Countryside Survey (CEH/NERC).

## Dataset structure and fields
- FILE: CS1990_98_07_Broad_Habitat_Change.csv
- Columns:
  - YEAR_FROM: Year of the starting survey
  - YEAR_TO: Year of the ending survey
  - LAND_CLASS: ITE Land Class code (Bunce et al. 1996; 1981; 2007)
  - BROAD_HABITAT: Broad Habitat code (1–17)
  - BROAD_HABITAT_NAME: Text name corresponding to the Broad Habitat
  - MEAN_CHANGE: Mean change in area (000s hectares) between the two years
  - LOWER_95PCT_LIMIT: Lower bound of 95% confidence interval (000s ha)
  - UPPER_95PCT_LIMIT: Upper bound of 95% confidence interval (000s ha)
  - SIG_5PCT: Significance at 5% level (Yes/No)
- Broad Habitat codes map to specific habitat types (e.g., Broad Habitat 1 = Broadleaved, Mixed and Yew Woodland; Broad Habitat 2 = Coniferous Woodland; … Broad Habitat 17 = Urban).
- All changes are national estimates derived from Countryside Survey data.

## Methodology and provenance
- Based on Countryside Survey data collected across Great Britain; national estimates generated from 1 km survey samples.
- Uses the 2007 ITE Land Classification for consistency in cross-year comparisons.
- Mapping and data handling procedures described in key references (Maskell et al., 2008; Barr 1990/1998; Bunce et al., 1996/2007; Scott 2007; Jackson 2000), with background on LAB classification and habitat mapping methodology.
- Data lineage and methodological context documented in accompanying CS publications and technical reports.

## Usage, attribution and licensing
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text required on copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data are provided for reuse under these attribution requirements; readers should consult the referenced materials for complete methodology and licensing details.

## References and related materials
- Core Countryside Survey outputs and methodological documents:
  - Countryside Survey: UK 2007 reports and technical papers (Carey et al.; Scott 2007; Bunce et al.; Maskell et al.)
  - ITE Land Classification of Great Britain 2007 (Bunce et al.)
  - Field Mapping and Habitat Mapping Methodology (Maskell et al.; Barr)
  - Guidance and definitions for Broad Habitat classifications (Jackson 2000)
- Links and DOIs provided in the original dataset documentation for the cited works.
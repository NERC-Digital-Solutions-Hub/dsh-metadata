# DATA HEADER INFORMATION for Root_carbon_stock_per_direct_measured_tree_pit_method.csv Please also see Manual_2_Belowground_Root_Survey.

## Overview
- The dataset presents biomass and carbon stock of tree roots.

## Variables and units
- site_ID: Text string; Information = P4GES WP4 site code.
- Subplot: Categorical; Information = subplot where the sample was collected; Unit = S1 / S2 / S3 / S4.
- Category_root: Categorical; Information = Category of root (Coarse Root CR or Medium Root MR); Unit = CR, MR.
- Biomasse: Numeric; Information = Biomass stock of Roots; Unit = Milligrams per hectare (Mg.ha-1).
- Root_C_Stock: Numeric; Information = Carbon stock of Roots; Unit = Mg.ha-1.

## Data provenance and access
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA; Project: P4GES
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo
- Related documentation: Manual_2_Belowground_Root_Survey

## Usage notes and caveats
- Potential unit inconsistency: Biomasse is described as Milligrams per hectare, while other conventions use Mg.ha-1 (Megagrams per hectare); verify unit alignment for analyses.
- Data coded by local site IDs and subplot categories; may require mapping to external geographies or standardized boundaries.
- Data appears at the subplot level; consider aggregation when comparing to site- or region-level datasets.

## Suggested analyses for Analysts
- Summarize total root biomass and root carbon stock by site_ID and by Category_root (CR vs MR).
- Explore relationships between Biomasse and Root_C_Stock to assess carbon density per unit biomass.
- Integrate with other ESPA/P4GES datasets to model drivers of belowground root stocks at fine spatial scales.
- Track data provenance and ensure proper acknowledgment in any derived work.
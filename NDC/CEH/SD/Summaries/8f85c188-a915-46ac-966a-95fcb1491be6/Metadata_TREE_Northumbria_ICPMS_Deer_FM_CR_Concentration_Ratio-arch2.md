# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- A dataset describing concentration ratios of elements in woodmouse tissue (fresh mass, whole body) divided by the dry mass of soil from co-located samples.
- Purpose aligns with environmental monitoring aims: demonstrate environmental condition and support scrutiny of health and policy performance over time.
- Intended for standardised outputs (reports, maps, charts) and for storage/portal upload of the underlying data.

## Key entities and metadata
- Latin_Species_Name / Common_Species_Name: taxonomic identifiers for the woodmouse used in the study.
- Site: sampling location.
- Date_Sample_Collected: date of sample collection.
- CEH_Sample_Description: description of the CEH (Centre for Ecology & Hydrology) sample.
- Notes: any additional sample observations or context.
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample paired with the woodmouse sample for ratio calculation.

## Concentration ratio fields
- For each element (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U):
  - Two possible columns are defined (e.g., V_Concentration_Ratio, 1 and V_Concentration_Ratio, 2), where:
    - Column 2 represents the Concentration Ratio itself: Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil.
    - Column 1 often contains a non-applicable marker (n/a) or is reserved for other representations.
  - Some entries include a less-than marker (e.g., <I, <Be, <Ni, <Ag, <U) indicating that the reported ratio is a threshold value rather than an exact measurement.
  - Units are typically n/a because these are ratios, not physical concentrations.

## Data quality and handling
- Data verification and quality assurance are implied steps prior to analysis.
- Data may be cleaned and transformed as part of standardised processing before outputting to reports, maps, or charts.
- The dataset should be stored in appropriate data portals as part of dataset management and dissemination.

## How this supports environmental monitoring
- Provides a standardised framework to compare metal/metalloid burdens in biota against soil exposure, enabling assessment of environmental contamination and transfer pathways.
- Facilitates cross-site and temporal analyses when combined with other monitoring data and datasets.
- Supports policy performance evaluation by offering consistent, interpretable concentration-ratio metrics.

## Challenges and opportunities for analysts
- Challenge: increasing the value of the dataset by integrating these concentration ratios with other environmental datasets (e.g., other species, abiotic sensors, land-use data) to enable broader health assessments.
- Challenge: ensuring easy access to the underlying data for downstream analysts and stakeholders.
- Opportunity: reuse of the dataset in dashboards, models, and comparative studies to strengthen environmental health insights and policy reviews.
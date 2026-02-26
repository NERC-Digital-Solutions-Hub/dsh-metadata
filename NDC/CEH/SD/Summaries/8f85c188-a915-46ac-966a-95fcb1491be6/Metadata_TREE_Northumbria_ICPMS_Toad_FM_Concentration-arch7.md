TREE_Northumbria_ICPMS_Toad_FM_Concentration

## Overview
- Dataset of ICP-MS–measured element concentrations in toads from Northumbria, with measurements on a fresh-mass basis (FM).

## Dataset structure and key fields
- Taxonomic and common names: Latin_Species_Name, Common_Species_Name
- Location and timing: Site, Date_Sample_Collected
- Sample identifiers: CEH_Sample_Code, CEH_Sample_Description
- Sample preparation context: Fresh_Mass_Ash_Mass_Ratio, Notes (preparation details, e.g., tissues sectioning)
- Concentration data: Element concentrations across a wide suite of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U)
- Units: mg/kg_FM (milligrams per kilogram fresh mass) for each element

## Concentration variables and data quality notes
- All element concentrations are reported on a fresh mass (FM) basis in mg/kg.
- Several field descriptions contain copy-paste errors (e.g., Mn/Fe/Co descriptions reference Cr; Fe and Mn entries may have incorrect text). Validate against the data values during use.
- The Notes column provides context related to toad preparation and tissue handling (e.g., whether separate tissues were prepared or not).

## Sampling and preparation details
- Sampling site and date capture spatial and temporal context for GIS analyses.
- CEH_Sample_Code and CEH_Sample_Description offer traceability to UKCEH sampling events.
- Fresh_Mass_Ash_Mass_Ratio provides information to interpret mass-basis conversions if needed.
- Notes document preparation specifics that may affect comparability across samples.

## GIS usage guidance
- Spatial analysis: map Concentration values by Site to identify geographic patterns of elemental accumulation.
- Temporal analysis: use Date_Sample_Collected to explore changes over time.
- Species-focused mapping: incorporate Latin_Species_Name and Common_Species_Name for species-specific visualizations.
- Data preparation: consider mass-basis implications (FM) and use Fresh_Mass_Ash_Mass_Ratio if converting to different mass bases.
- Data quality: account for potential labeling issues in the metadata (verify field descriptions against data) and apply QA checks before visualization.
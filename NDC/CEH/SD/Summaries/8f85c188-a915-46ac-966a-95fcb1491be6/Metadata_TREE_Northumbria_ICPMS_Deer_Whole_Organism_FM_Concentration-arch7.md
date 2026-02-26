# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

## Overview
- Dataset of deer whole-organism concentrations collected from Northumbria (UKCEH context) using ICP-MS.
- Intended for GIS-based visualization and spatial analysis of contaminant concentrations across sampling sites.
- Includes both sample metadata and concentration measurements across a wide range of elements.

## Metadata fields (describing samples and context)
- Latin_Species_Name: Latin name of the deer species.
- Common_Species_Name: Common name of the deer species.
- Site: Sampling site location (geographic relevance for GIS mapping).
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Codes: UKCEH sample codes.
- CEH_Sample_Description: UKCEH sample description.
- Notes: Notes related to tissues used to calculate deer whole-organism concentrations.

## Concentration data structure
- Concentration variables are listed for numerous elements, reported as mg/kg (fresh mass, FM, or whole-organism FM).
- Key pattern: element concentration fields named with suffixes like _FM (fresh mass) or _whole-organism_FM.
- Examples of elements covered:
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Some elements have paired fields (1 and 2), indicating multiple measurements or sub-samples (e.g., Ba_mg_kg_whole- organism _FM, 1 and Ba_mg_kg_whole- organism _FM, 2).
- Less-than values are indicated for certain columns with markers like <Be, <Al, <Ni, <Mo, <Ag, <U to denote concentrations reported as below detection or threshold.

## Data formats and units
- Units: mg/kg (milligrams per kilogram).
- Fresh mass vs. whole-organism fresh mass interpretations are specified via field naming (e.g., _FM, fresh mass).
- Be, Al, Ni, Mo, Ag, U may include less-than markers.
- Some typographical inconsistencies are present in field names (e.g., spacing in “whole-organism _FM” vs “whole-organism_FM”), which should be reconciled during data cleaning.

## GIS-oriented use and integration
- Enables creation of map layers showing spatial distribution of contaminant concentrations across deer samples.
- Can be joined to site coordinates and other spatial attributes for display (e.g., choropleth or graduated symbol maps for element concentrations).
- Notes field provides essential information about tissue type, ensuring correct attribution of concentrations to whole-organism measurements.

## Data quality considerations and challenges
- Data cleaning needed to standardize field names and resolve inconsistencies.
- Handling of multi-field concentration entries (1/2) and their interpretation in analysis.
- Management of below-detection values (<) in statistical summaries and visualizations.
- Integration with other datasets requires careful alignment of site identifiers, sampling dates, and tissue notes.
- Ensuring consistency of units and mass definitions across all concentration fields for reliable GIS analysis.

## Practical guidance for GIS specialists
- Verify site-level coordinates and ensure proper georeferencing for each sampling site.
- Use the Notes field to confirm tissue types and calculation methods for whole-organism concentrations.
- Treat "<" values appropriately in analyses (e.g., censoring or imputation) and document handling rules.
- Maintain consistent field naming conventions during data import to avoid misalignment across element columns.
- Consider creating separate GIS layers or symbolization schemes for different element groups (e.g., essential elements vs. contaminants) and for presence of below-detection values.
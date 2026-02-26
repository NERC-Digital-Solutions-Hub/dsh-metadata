# TREE_Northumbria_ICPMS_Toad_AM_Concentration

## Overview
- Dataset of ICP-MS elemental concentrations in toad ash (AM), with associated sampling metadata.
- Includes both Latin and common names of species, sampling site, date, UKCEH sample codes and descriptions, and preparation notes.
- Concentrations are reported for a wide suite of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) measured as mg/kg in ash mass.
- A key sample descriptor is Fresh_Mass_Ash_Mass_Ratio, indicating the ratio of whole-organism fresh mass to ash mass.

## Data Structure
- Core identifiers and metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description
  - Notes related to toad preparation
- Preparation and sample characteristics:
  - Fresh_Mass_Ash_Mass_Ratio
- Element concentration fields (all in mg/kg in ash mass):
  - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM, P_mg_kg_AM, K_mg_kg_AM, Ca_mg_kg_AM, Ti_mg_kg_AM, V_mg_kg_AM, Cr_mg_kg_AM, Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM, Cu_mg_kg_AM, Zn_mg_kg_AM, As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM, Sr_mg_kg_AM, Mo_mg_kg_AM, Ag_mg_kg_AM, Cd_mg_kg_AM, Cs_mg_kg_AM, Ba_mg_kg_AM, Tl_mg_kg_AM, Pb_mg_kg_AM, U_mg_kg_AM
- Notes on data quality/representation:
  - Some field descriptions show inconsistent formatting (e.g., Units = n/a) and minor typographical irregularities in element field definitions.

## Data Quality and Gaps
- Metadata completeness varies; ensure species names, site identifiers, and sample codes are consistent for GIS joins.
- Unit consistency is primarily mg/kg in ash mass, but some fields show ambiguous or missing unit metadata.
- Data may be dispersed across multiple sources; validate CEH sample codes against a master list.
- Some fields contain formatting artifacts that should be cleaned prior to GIS integration.

## How This Data Supports GIS Work
- Spatial analysis: Site column enables joining to GIS point/ polygon layers to map metal accumulation by location.
- Temporal analysis: Date_Sample_Collected supports time-series visualization when multiple sites have repeated sampling.
- Multivariate mapping: Element concentration fields allow creation of choropleth maps or composite indices (e.g., metal load indices) for environmental risk assessment.
- Metadata-rich: Sample descriptions and preparation notes aid in data provenance and in documenting methodology within GIS projects.

## Recommended GIS-Readiness Steps
- Clean and standardize field names (e.g., convert I_mg_kg_AM to I_mg_per_kg_AM) and ensure uniform units (mg/kg_ash_mass).
- Resolve any inconsistencies in Site identifiers and link to a spatial dataset (locations, extents, coordinate reference system).
- Create a metadata header in the GIS dataset with provenance, sampling dates, and CEH sample codes.
- Validate data quality (range checks, missing values) for each element concentration field.

## Visualization and Analysis Ideas
- Per-site choropleth maps showing individual element concentrations (select elements of interest).
- Multi-element heat maps or spider/radar plots per site or per species.
- Time-series dashboards showing trends in key elements by site (if repeated sampling exists).
- Spatial overlays with pollution sources, land use, or geology to explore relationships with metal concentrations.

## Key Considerations for GIS Stakeholders
- Ensure alignment between site naming in this dataset and the GIS site layer to enable accurate joins.
- Maintain a clear master schema for fields to support cross-project reuse (e.g., standardize element field names).
- Document data provenance and any preprocessing steps to support reproducibility in map products.
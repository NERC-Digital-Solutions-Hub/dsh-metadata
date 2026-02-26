# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)

## Overview
- This document is a supplement to the supporting documentation for data series described in Turf2Surf_WP2_Supporting_documentation.rtf.
- It describes soil carbon data for the Conwy catchment in North Wales from 2013 and 2014, as detailed in the table Turf2Surf_Soil_data.csv.
- The dataset focuses on soil physical, chemical, and biological measurements alongside plant-related data, within the Turf2Surf project data framework.

## Dataset structure and scope
- The dataset contains 644 rows and 48 additional columns beyond the first nine shared fields.
- The first 9 columns are common across several related datasets and include:
  - Unique Site number (as introduced in related documentation)
  - Habitat and a detailed Habitat description
  - Site name
  - Ecosystem component (Plant, Soil, or Roots)
  - If the component is Plant, the species information is provided; otherwise NA
  - Plot number (1–4) and Replicate number
  - Soil depth interval for Soil and Roots components
- Missing values are indicated with NA, arising from limitations such as restricted soil depths or fewer replicates.
- Root measurements were taken at fewer sites than other components.

## Content of the additional columns (examples)
- The dataset includes a wide range of soil and phosphorus-related measurements, with 48 extra columns such as:
  - Loss on ignition (LOI) and LOI-C (carbon in LOI fraction) in % dry weight
  - Soil water content (% fresh weight)
  - Bulk density (g cm^-3 per dry soil weight)
  - pH (in water) and Electrical conductivity (µS cm^-1)
  - Soil nitrate and soil ammonium (mg N per litre)
  - Exchangeable cations: sodium, potassium, calcium (meq kg^-1 dry soil)
  - Olsen phosphorus and several extractable/available phosphorus pools (e.g., CaCl2-extractable P, citrate-extractable P, enzyme-extractable P, HCl-extractable P)
  - Dissolved organic carbon (mg C per litre)
  - Total dissolved nitrogen (mg N per litre)
  - Total soil carbon (%) and total soil nitrogen (%)
  - Root biomass (g m^-2) and fine root biomass (g m^-2)
  - A broad set of extractable elemental measurements (Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U, etc.) with various units (e.g., mg per kg dry soil, mg L^-1)
- Each phosphorus-related column is described with the contextual meaning of the extractable pool (e.g., fractions emulating plant and microbial access).

## Data quality and notes
- NA entries indicate measurements not performed for a given site.
- Root measurements are less frequently collected, reflecting site-specific sampling limitations.
- The dataset is designed to support cross-dataset consistency, with the common first nine fields facilitating linkage to other Turf2Surf datasets.

## Relevance for monitoring and governance
- The structured data dictionary and extensive metadata (including units and descriptions) support quality assurance, data transformation, and clear communication of findings.
- The breadth of soil carbon and phosphorus fractions enables evaluation of soil health, carbon budgeting, and nutrient availability across sites and habitats.
- The explicit handling of missing data and partial measurements informs transparent reporting and data governance decisions.
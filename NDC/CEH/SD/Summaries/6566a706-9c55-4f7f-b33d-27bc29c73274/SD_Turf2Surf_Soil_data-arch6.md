# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil_data.csv

## Overview
- Supplement to the supporting documentation for Turf2Surf data series (WP2).
- Details the data structure for soil carbon data in the Conwy catchment, North Wales, spanning 2013 and 2014.
- The dataset contains 644 rows and 48 additional columns beyond the first 9 common columns.
- NA indicates missing values (e.g., data not available due to restricted depth, limited replicates, or unperformed measurements).

## Shared first 9 columns (common across several Turf2Surf datasets)
- A: Site number (unique identifier, as introduced in Table 1 of the supplementary documentation).
- B: Habitat
- C: Habitat description (more detail)
- D: Site name
- E: Ecosystem component (Plant, Soil, or Roots)
- F: If Plant, the species; otherwise NA
- G: Plot number (1 to 4)
- H: Replicate number (used when photosynthesis measurements were not co-located with plots)
- I: Soil depth interval (for Soil and Roots components)

## Data content and structure
- NA values indicate data not available (e.g., restricted soil depths or limited replicates).
- The dataset has 48 additional columns beyond the initial 9, totaling 48 columns with detailed measurements.

## 48 additional columns: key categories and examples
- J: LOI (Loss on ignition); Unit: % dry weight; Description: Loss on ignition
- K: LOI-C; Unit: % dry weight; Description: Carbon in the LOI fraction
- L: Soil water content; Unit: % fresh weight
- M: Bulk density; Unit: g cm^-3 per dry weight of soil
- N: pH; Unit: in water
- O: Electrical conductivity; Unit: µS cm^-1
- P: Soil nitrate; Unit: mg nitrate-N per liter
- Q: Soil ammonium; also described as soil available ammonium
- R: Exchangeable sodium; Unit: meq per kg dry soil
- S: Exchangeable potassium; Unit: meq per kg dry soil
- T: Exchangeable calcium; Unit: meq per kg dry soil
- U: Olsen phosphorus; Unit: mg PO4-P per kg dry soil
- V: CaCl2 extractable phosphorus; Unit: mg PO4-P per kg dry soil
- W: Citric acid extractable phosphorus; Unit: mg PO4-P per kg dry soil
- X: Enzyme extractable phosphorus; Unit: mg PO4-P per kg dry soil
- Y: Hydrochloric acid extractable phosphorus; Unit: mg PO4-P per kg dry soil
- Z: Dissolved organic carbon; Unit: mg carbon per liter
- AA: Total dissolved nitrogen; Unit: mg nitrogen per liter
- AB: Total soil carbon; Unit: %
- AC: Total soil nitrogen; Unit: %
- AD: Root biomass; Unit: g m^-2
- AE: Fine root biomass; Unit: g m^-2
- AF to BE: A series of extractable phosphorus-related and elemental measurements (e.g., Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U) with corresponding units and descriptions as extractable or measured parameters
- NA: Stated that measurements were not performed for a given site; root measurements were taken at fewer sites

## Usage notes
- The first 9 columns are shared with related datasets (e.g., plant structural measurements and biomass datasets) to facilitate cross-dataset analysis and self-serve exploration.
- Data requires careful handling due to missing values (NA) and, for root measurements, the smaller number of sites.
- This structure supports analyses of soil carbon fractions, nutrient pools, and related soil chemistry variables across sites and depths.
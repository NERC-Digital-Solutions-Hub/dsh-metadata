# Details of data structure for the dataset Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil_data.csv

## Overview
- Supplement to the supporting documentation for Turf2Surf data series (Turf2Surf_WP2_Supporting_documentation.rtf)
- Focus on soil carbon data in the Conwy catchment, North Wales, for 2013 and 2014
- Several related datasets share the first 9 columns to support cross-dataset compatibility (plant, biomass, soil, and root measurements)

## Data structure and scope
- Core structure: the first 9 columns are common across multiple related datasets
- Dataset size: 644 rows with 48 additional columns beyond the first 9
- Missing data: missing values are indicated as NA (e.g., restricted depths, limited replicates, or outliers)
- Root measurements: taken at fewer sites; some columns may not have data for all sites

## Shared first 9 columns (described by letter)
- A: Unique site number (as introduced in related documentation)
- B: Habitat
- C: Detailed Habitat description
- D: Site name
- E: Ecosystem Component (plant, soil, or roots)
- F: Plant species (if Ecosystem Component = Plant); otherwise NA
- G: Plot number (1 to 4)
- H: Replicate number (used when measurements were not co-located with plots)
- I: Soil depth interval (for components Soil and Roots)

## 48 additional columns (data types and example content)
- J: LOI (Loss on ignition); Unit: % dry weight
- K: LOI-C (Carbon in the LOI fraction); Unit: % dry weight
- L: Soil water content; Unit: % fresh weight
- M: Bulk density; Unit: g cm-3 per dry weight of soil
- N: pH; Unit: nH2O
- O: Electrical conductivity; Unit: µS cm-1
- P: Soil nitrate; Unit: mg nitrate-N per litre
- Q: Soil ammonium; Unit: mg ammonium-N per litre
- R, S, T: Exchangeable sodium, potassium, calcium; Unit: meq per kg dry soil
- U: Olsen phosphorus; Unit: mg PO4-P per kg dry soil
- V: Calcium chloride extractable phosphorus; Unit: mg PO4-P per kg dry soil
- W: Citric acid extractable phosphorus; Unit: mg PO4-P per kg dry soil
- X: Enzyme extractable phosphorus; Unit: mg PO4-P per kg dry soil
- Y: Hydrochloric acid extractable phosphorus; Unit: mg PO4-P per kg dry
- Z, AA, AB, AC: Dissolved organic carbon; Total dissolved nitrogen; Total soil carbon; Total soil nitrogen; Units vary by parameter
- AD: Root biomass; Unit: g m-2
- AE: Fine root biomass; Unit: g m-2
- AF–AU (and onwards): Extractable phosphorus fractions and elemental contents (examples: Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U); Units vary by element/term
- NA values: Indicate measurements not performed for that site
- Root measurements note: Root-related columns were measured at a subset of sites

## Data governance and usability considerations
- Cross-dataset compatibility: shared first 9 columns facilitate integration with other Turf2Surf data series
- Metadata richness: extensive column-level descriptions (J–AU range) support data discovery and understanding of each measurement
- Data quality considerations: presence of NA values highlights gaps in measurement coverage and potential data gaps to address in analyses
- Applicability: suitable for analyses of soil carbon and nutrient pools, phosphorus fractions, soil chemistry, and root-related biomass across sites in the Conwy catchment for 2013–2014
- Documentation linkage: described as a supplement to WP2 supporting documentation, indicating alignment with broader data governance and documentation standards
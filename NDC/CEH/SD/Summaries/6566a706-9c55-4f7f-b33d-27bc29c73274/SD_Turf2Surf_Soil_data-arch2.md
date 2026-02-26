# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)

## Purpose and scope
- Supplement to the supporting documentation for Turf2Surf data series.
- Details the data structure for the Soil carbon dataset in the Conwy catchment (North Wales) for 2013 and 2014, as described in Turf2Surf_Soil_data.csv.

## Datasets sharing the first nine columns
- Plant structural measurements in North Wales and Northwest England (2013 and 2014).
- Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014).
- Soil physical, chemical and biological measurements in the Conwy catchment (2013 and 2014).
- Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016).
- Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014).

## Data schema: key columns (A–I)
- A: Unique Site number (as introduced in Table 1 of the supplementary documentation).
- B–C: Habitat and detailed Habitat description.
- D: Site name.
- E: Ecosystem Component (Plant, Soil, or Roots).
- F: If Component is Plant, the plant species; otherwise NA.
- G–H: Plot number (1–4) and Replicate number (used when photosynthesis measurements are not co-located with plots).
- I: Soil depth interval for Soil and Roots components.
- Missing values are indicated as NA (due to restrictions on depths, replicates, or outliers).

## Dataset size
- 48 additional columns beyond the first nine.
- 644 rows total.

## Example of the 48 additional columns (selected categories)
- J: LOI (Loss on ignition) — % dry weight; K: LOI-C — % dry weight (carbon in LOI fraction); L: Soil water content — % fresh weight; M: Bulk density — g cm^-3 (per dry soil weight, for the indicated depth interval); N: pH (in H2O); O: Electrical conductivity (µS cm^-1); P: Soil nitrate — mg nitrate-N per litre; Q: Soil ammonium — mg ammonium-N per litre; R–T: Exchangeable Na, K, Ca — meq per kg dry soil; U: Olsen phosphorus — mg PO4-P per kg dry soil; V–AY: Various extractable phosphorus fractions (CaCl2-P, citrate-P, enzyme extractable P, HCl extractable P, and numerous related extractables), plus a broad suite of element concentrations (Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U) across multiple extractable measures.
- Z–AU: Additional extractable phosphorus metrics and related soil chemical measurements (as listed; includes dissolved organic carbon/nitrogen and bulk soil carbon/nitrogen concepts).

Note: NA indicates measurements not performed for that site. Root measurements were taken at fewer sites.

## Data quality and handling
- Missing values present (NA) due to limited soil depths, limited number of soil cores/replicates, or outliers.
- Root data exist but are less complete across sites.

## How this fits into environmental monitoring work
- Provides a standardized data structure and extensive soil chemical measurements linked to site-specific habitat and plot information.
- Supports consistent analyses of soil carbon and related soil properties across sites and years (2013–2014).

## Analytical and data management implications for analysts
- Data verification, quality assurance, cleaning, and transformation are required before analysis.
- Outputs can be presented as reports, maps, and charts, with datasets stored and uploaded to appropriate portals.
- Opportunities to increase dataset value by combining with other monitoring data and enabling access to underlying data used for outputs.
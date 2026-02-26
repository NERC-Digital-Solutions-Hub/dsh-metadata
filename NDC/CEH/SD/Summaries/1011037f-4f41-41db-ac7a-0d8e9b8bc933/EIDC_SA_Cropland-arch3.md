# The data included in Croplands_2050.csv relates to an analysis of the impact changes in water availability will have on cropland availability in 2050

## Aim
- Combine projections of water scarcity with current cropland extent to identify country-level vulnerabilities of cropland to water scarcity in 2050.

## Data sources and collection methods
- Global maps of:
  - Change in annual runoff (%) and
  - Water scarcity index (1 = not water scarce to 4 = severely water scarce)
  - Derived from projections from five general circulation models (GCMs) provided by N. Arnell (University of Reading); methodology described in Arnell et al. 2011.
- Global cropland extent maps downloaded from Earthstat (Monfreda et al. 2008; Ramankutty et al. 2008); data on a global 5 arc-minute grid, derived from satellite data and census statistics.

## Experimental design / Sampling regime
- Desk-based study overlaying cropland maps with hydrological projections to identify country-level vulnerability.

## Calibration steps and values
- No calibration required; all data were published previously (section 2).

## Analytical methods
- Overlay cropland with GCM-specific projections of water scarcity and annual runoff using ArcGIS (spatial overlays).
- Define land as vulnerable if cropland falls within areas that (i) show declining runoff and (ii) are within water-scarce watersheds.
- Calculate the percentage of cropland within a country that meets both criteria.

## Nature and units of recorded values
- Croplands_2050.csv: percentage of total cropland area in each country classified as vulnerable.
- Country names aligned with FAOSTAT conventions.
- Runoff change reported as percentage; water scarcity on a 1–4 scale; cropland areas in hectares.

## Quality control
- Datasets used were sourced directly from data owners to ensure no modified versions were used.

## Details of data structure
- Country-level estimates averaged across five GCMs.
- Includes standard deviation across the GCM ensemble.

## Data sources and references (underlying data sets)
- Hydrological models (GCMs): CSIRO Mk3, HADGEM, INMCM4, IPSL M.R, MRIOC_CM3.
- Water resources and climate context: Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010.
- Cropland maps: Monfreda et al. 2008; Ramankutty et al. 2008.
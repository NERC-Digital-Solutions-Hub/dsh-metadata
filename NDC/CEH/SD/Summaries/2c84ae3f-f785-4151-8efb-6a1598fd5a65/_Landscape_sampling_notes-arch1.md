# Summary Experimental Design/Sampling Regime

- Purpose: Document the experimental design and field sampling regime used to study earthworm communities across hedges, margins, and different land uses, enabling downstream analysis of abundance, biomass, species composition, and functional groups.

## Study sites and land use
- Little Langton (LL)
  - A1: organic arable
  - A2: conventional arable
  - B1: organic ley (grass with cattle)
  - B2: organic arable (ploughed; few visible growth at sampling)
- Hutton Wandesley (HW)
  - A1: conventional ley
  - B: conventional arable
- Overton (OV)
  -  Conventional arable
- Whenby (WH)
  - A: organic ley
  - B: organic arable
- Each site involves single transects per field, with hedges maintained for sampling along a gradient from hedge into the field.

## Sampling design and transects
- Transects run at 90 degrees from hedge into the field, located midway along field length where possible.
- Paired transects:
  - WH and HW: located in appropriate fields for direct comparison.
  - OV and LL: transects positioned on opposite sides of the hedge.
- Start points chosen where hedge condition was good.
- Distances from hedge: 0 m (hedge) and 2, 4, 8, 16, 32, 64 m into fields; margin samples labeled as Margin (M) and hedge samples as Hedge (H).

## Field methods and instrumentation
- Soil pits: 18 x 18 x 15 cm excavated along each transect at hedge, margin, then at 2, 4, 8, 16, 32, 64 m.
- Earthworm extraction: mustard solution (dilute allyl isothiocyanate) poured into pits to collect emerging earthworms; specimens preserved in ethanol.
- Identification: using Sims and Gerard field studies key.
- Measurements at each pit:
  - Soil moisture: three readings in mV at 5 cm and 10 cm depths using ML3 ThetaProbe
  - Soil temperature: 5 cm and 10 cm depths
  - Soil bulk density: 5 cm and 15 cm depths (steel bulk density rings, 118 cm3)
- Sample types: abundance/count (A) and biomass (B)

## Data collected and structure
- Recorded values per pit:
  - Number of earthworms
  - Biomass (grams)
  - Distance from hedge (metres)
  - Designation: Hedge (H) or Margin (M)
  - Depth category: Mustard (P) vs Topsoil (S)
- Data files (Earthworm landscape datasets) include:
  - HWA1_EW_landscape.csv
  - HWB_EW_landscape.csv
  - LLA1_EW_landscape.csv
  - LLA2_EW_landscape.csv
  - LLB1_EW_landscape.csv
  - LLBS_EW_landscape.csv
  - OV7_EW_landscape.csv
  - WHA_EW_landscape.csv
  - WHB_EW_landscape.csv
- Each file contains about 30 columns:
  - Date, Field, Transect, Distance, Depth, Sample type
  - Code (sample code)
  - Species- and biomass-specific columns
  - Species list covers endogeic, epigeic, and anecic groups (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)
- Depth/position coding:
  - H indicates sample from below hedge; M indicates sample from field margin
  - Depth: Mustard (P) vs Topsoil (S)
- Species and abundance/biomass data organized by species code and taxonomic group (endogeic, epigeic, anecic)

## Landscape soil data (physicochemical context)
- Landscape2016_soil_data.csv includes 14 columns:
  - Date, field name, code, distance_m
  - Moisture readings at 5 cm and 10 cm depths (three replicates a, b, c) in millivolts
  - Soil temperatures at 5 cm and 10 cm depths (°C)
  - Soil bulk density at 5 cm and 15 cm depths (g/cm3)
- Purpose: provide concurrent soil context for earthworm distributions and functional groups

## Earthworm taxonomy and functional groups
- Functional groups:
  - Endogeic: soil-living, horizontal burrows
  - Epigeic: litter-living
  - Anecic: soil-living, deep vertical burrows
- Species mapping includes common UK earthworms (e.g., Allolobophora spp., Aporrectodea spp., Dendrodrilus rubidus, Eisenia fetida, Lumbricus spp., Murchieona muldali, Satchellius mammalis) and placeholders for damaged or immature individuals (END-dm, EPI-im, etc.)

## Data quality, provenance, and usage notes
- Data designed for analyses of hedge-margin effects, land-use impacts, and distance-from-hedge gradients on earthworm communities (by abundance, biomass, and species/functional group composition).
- Data collection and identification rely on field notes, standardized pit sampling, mustard extraction, and Sims & Gerard key, with ethanol preservation for voucher-like specimens.
- Some records may contain blank cells (no data for certain species or measurements).
- Data can be combined with soil context (moisture, temperature, bulk density) for multivariate analyses.

## References and provenance
- Earthworms taxonomy and references follow Sims & Gerard (1999).
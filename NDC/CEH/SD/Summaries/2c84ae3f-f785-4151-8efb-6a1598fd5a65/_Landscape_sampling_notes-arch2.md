# Summary Experimental Design/Sampling Regime

- Aim and context
  - Document describes a standardized field and lab protocol to monitor soil health via earthworm diversity, abundance, and biomass across hedgerow-adjacent fields.
  - Focus on consistent data collection to support environmental health assessments and policy performance over time.
  - Data management goals include verification, quality assurance, cleaning, transformation, storage, and portal upload; aligns with broader monitoring responsibilities.

- Study sites and land use
  - Sites include Little Langton (LL), Hutton Wandesley (HW), Overton (OV), Whenby (WH), with multiple land-use types:
    - Organic arable (A1, A2)
    - Conventional arable (A2)
    - Organic ley (B1)
    - Organic arable/ley combinations (B2)
  - Sampling dates in May 2016; hedges used as sampling boundaries; paired transects used for comparison in some sites.

- Experimental design
  - Transects
    - One transect per site, laid out at 90 degrees from the hedge into the field.
    - Paired transects used for site comparisons (WH/HW; OV/LL).
    - Transects begin where hedge condition is good.
  - Distances and pit locations
    - Soil pits excavated along the transect at hedge, margin, and at 2, 4, 8, 16, 32, and 64 metres into the field.
  - Sample types and coding
    - Hedge (H) samples taken below hedges; Margin (M) samples taken from field margins.
    - Depth codes: Mustard (P) and Topsoil (S).
  - Collection and analysis methods
    - Earthworms collected by hand sorting from soil pits, then extracted with mustard solution (dilute allyl isothiocyanate) and preserved in ethanol.
    - Identification using Sims and Gerard Field Studies key.
    - Measurements taken at each pit: soil moisture (three readings at 5 cm and 10 cm, in millivolts with ML3 ThetaProbe), soil temperature (5 cm and 10 cm with Checktemp1), soil bulk density (5 cm and 15 cm using 118 cm3 rings; oven-dried for density).

- Data collected and units
  - Recorded values
    - Number of earthworms
    - Biomass (grams)
    - Distance from hedge (metres)
  - Sample indicators
    - H indicates sample from below hedge; M indicates sample from field margin
  - File structure
    - Land-ecology earthworm datasets: HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv
    - Each file contains ~30 columns with: Date, Field, Transect, Distance, Depth (Mustard or Topsoil), Sample type (A = abundance, B = biomass), followed by species-specific counts/biomass or a blank if no data.
  - Earthworm taxonomy and functional groups
    - Species mapped to functional groups: Endogeic (soil-living, horizontal burrows), Epigeic (litter-living), Anecic (deep vertical burrows)
    - Species list includes Allolobophora chlorotica, Allolobophoridella eiseni, Aporrectodea caliginosa, Aporrectodea caliginosa nocturna, Aporrectodea limicola, Aporrectodea longa, Aporrectodea rosea, Dendrodrilus rubidus, Eisenia fetida, Eiseniella tetraedra, Lumbricus castaneus, Lumbricus festivus, Lumbricus rubellus, Lumbricus terrestris, Murchieona muldali, Octolasion cyaneum, Octolasion tyrtaeum, Satchellius mammalis, plus damaged/immature categories (END-dm, EPI-dm, ANE-dm, END-im, EPI-im, ANE-im).
  - Landscape soil data
    - Landscape2016_soil_data.csv comprises 14 columns: Date, field name, code, distance_m, moisture_mV_5_cm_depth_a/b/c, moisture_mV_10_cm_depth_a/b/c, soil temp at 5 cm and 10 cm, soil bulk density at 5 cm and 15 cm.
  - Miscellaneous and references
    - Earthworm functional groups and species associations provided; reference: Sims & Gerard (1999).

- Data management and access considerations
  - Emphasis on quality assurance, standardised methodologies, and clear data structure to facilitate downstream analysis and cross-study comparisons.
  - Challenges highlighted include increasing dataset value through data integration with other datasets and improving access to underlying data used to generate outputs.
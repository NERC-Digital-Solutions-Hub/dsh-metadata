# Summary Experimental Design/Sampling Regime

- Purpose and scope
  - Document detailing the experimental design, sampling regime, and data structure for earthworm and soil measurements across multiple arable and hedgerow landscapes in 2016.
  - Aims aligned with standardized monitoring: consistent data collection to enable environmental health assessments and policy-relevant analyses.

- Study sites and land use
  - Little Langton (LL)
    - A1: organic arable
    - A2: conventional arable
    - B1: organic ley
    - B2: organic arable
  - Hutton Wandesley (HW)
    - A1: conventional ley
    - B: conventional arable
  - Overton (OV)
    - Conventional arable
  - Whenby (WH)
    - A: organic ley
    - B: organic arable
  - Each site includes transects positioned relative to hedges and field margins for paired comparisons where noted.

- Sampling design and pairing
  - Number of transects per site: 1
  - Transects oriented at 90 degrees from hedge into the field; paired transects used to compare corresponding land-use types (e.g., A1 paired with A2; B1 paired with B2).
  - Locations chosen relative to hedge condition (start from hedge with good condition) and, for some sites, on opposite sides of the hedge.
  - For LL, explicit pairings:
    - A1 paired with A2
    - B1 paired with B2

- Fieldwork methodology
  - Soil pits: 18 cm x 18 cm x 15 cm, excavated along the transect at hedge, margin, and at distances of 2, 4, 8, 16, 32, and 64 meters from the hedge.
  - Earthworm extraction: Mustard solution (dilute allyl isothiocyanate) used to stimulate earthworms from pits; collected specimens preserved in ethanol and identified with Sims and Gerard Field Studies key.
  - Soil and environmental measurements at each pit:
    - Soil moisture: three readings in millivolts (mV) at 5 cm and 10 cm depths using ML3 ThetaProbe
    - Soil temperature: measurements at 5 cm and 10 cm using Checktemp1
    - Soil bulk density: measured at 5 cm and 15 cm depths using 118 cm3 rings; density calculated on a dry basis

- Data collected and recorded values
  - Earthworm data: counts (abundance) and biomass (grams)
  - Distance from hedge: measured in metres
  - Sample origin indicator: H = hedge, M = field margin
  - Depth indicator: P = mustard sample, S = topsoil sample
  - Temporal coordinates: sampling date per site

- Data files and structure
  - Earthworm landscape data (30 columns per file), example files:
    - HWA1_EW_landscape.csv
    - HWB_EW_landscape.csv
    - LLA1_EW_landscape.csv
    - LLA2_EW_landscape.csv
    - LLB1_EW_landscape.csv
    - LLBS_EW_landscape.csv
    - OV7_EW_landscape.csv
    - WHA_EW_landscape.csv
    - WHB_EW_landscape.csv
  - Key data fields within these files:
    - Date, Field (field name abbreviation), Transect, Distance (m from hedge), Depth (Mustard P or Topsoil S), Sample type (A = abundance/count, B = biomass in grams)
    - Species codes and names (e.g., Al-chl Allolobophora chlorotica; Ad-esi Allolobophoridella eiseni; Ap-cal Aporrectodea caliginosa; etc.)
    - End-dm, EPI-dm, ANE-dm, END-im, EPI-im, ANE-im indicators for functional/damaged status
  - Landscape dataset for soil measurements (14 columns):
    - Landscape2016_soil_data.csv
    - Columns include Date, Field, code, Distance_m, Hedge/Margin indicator, Depth, moisture_mV_5_cm_depth_a/b/c, moisture_mV_10_cm_depth_a/b/c, Soil_temp_5_cm, Soil_temp_10_cm, Soil_bulk_density_5_cm, Soil_bulk_density_15_cm

- Measurements and units (earthworms and soil)
  - Earthworm metrics: number of individuals (counts) and biomass (grams)
  - Distances: metres from hedge
  - Depth indicators: Mustard (P) and Topsoil (S)
  - Soil moisture: millivolts (mV)
  - Soil temperature: degrees Celsius
  - Soil bulk density: grams per cubic centimeter (g/cm3)
  - Taxonomic and functional grouping available (Endogeic, Epigeic, Anecic)

- Earthworm taxonomy and functional groups
  - Endogeic (soil-living, horizontal burrows)
  - Epigeic (litter-living)
  - Anecic (soil-living, deep vertical burrows)
  - Species mapping included (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)
  - Codes designate both species and functional/damage status (e.g., END-dm, EPI-im)

- Data quality and references
  - Methods follow standardized earthworm sampling protocols, including mustard extraction and key-based identification
  - Reference: Sims & Gerard (1999)

- Data accessibility and purpose for analysts
  - Data are organized in structured CSV files enabling cross-site comparisons
  - Variables include field-scale environmental data (soil moisture, temperature, bulk density) to support monitoring of soil biodiversity and health in relation to land-use practices and hedge/margin ecology
  - Designed to be stored and accessible via appropriate data portals consistent with monitoring responsibilities and data-quality expectations
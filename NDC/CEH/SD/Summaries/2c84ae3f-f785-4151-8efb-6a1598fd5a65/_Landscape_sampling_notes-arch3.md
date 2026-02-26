# Summary Experimental Design/Sampling Regime

- Objective and scope
  - Document describes a field-based monitoring regime to assess earthworm populations as indicators of soil health across multiple agricultural landscapes.
  - Aims to capture spatial patterns relative to hedges and field margins, across different land uses.

- Study sites and land uses
  - Little Langton (LL): transect-based sampling with multiple land uses including organic arable (A1), conventional arable (A2), organic ley (B1), and organic arable (B2).
  - Hutton Wandesley (HW): two sites/routes—conventional ley (HWA1) and conventional arable (HWB).
  - Overton (OV): conventional arable (OV7).
  - Whenby (WH): organic ley (WHA) and organic arable (WHB).
  - Each site features a single transect per sampled hedge/field edge, with paired transects in some comparisons (e.g., WH and HW).

- Experimental design and field methods
  - Transect layout: one transect laid out at 90 degrees from the hedge into the field; located mid-field where possible.
  - Paired designs: where applicable, transects are paired to compare hedge-side versus field interior conditions (e.g., OV, LL; WH/HW pairings).
  - Sampling points along transects: hedge (or margin) and successive depths at 2, 4, 8, 16, 32, and 64 meters from the hedge.
  - Soil pit method: soil pits (18 x 18 x 15 cm) excavated along the transect (hedge, margin, then increasing distance).
  - Earthworm collection: earthworms extracted using dilute mustard solution; specimens preserved in ethanol and identified using the Sims and Gerard (Field studies) key.

- Data collection details and measurements
  - Earthworm data: number of individuals and biomass (grams) per pit; depth markers indicate whether collected from hedge or margin samples.
  - Soil and site context: at each pit, additional measurements taken include soil moisture (three readings at 5 cm and 10 cm depths, recorded in millivolts via a ThetaProbe), soil temperature (5 cm and 10 cm depths), and soil bulk density (5 cm and 15 cm depths using bulk density rings; density calculated on an oven-dry basis).

- Data structure and units
  - Recorded values include:
    - Number of earthworms
    - Biomass (grams)
    - Distance from hedge (metres)
    - Hedge (H) or Margin (M) designation for sample origin
  - Depth indicator codes: Mustard (P) for mustard pit samples versus Topsoil (S) for surface samples
  - Files use consistent headers and coding to enable cross-site comparability

- Data structure and files
  - Earthworm landscape data files (30-column structures) with names such as:
    - HWA1_EW_landscape.csv
    - HWB_EW_landscape.csv
    - LLA1_EW_landscape.csv
    - LLA2_EW_landscape.csv
    - LLB1_EW_landscape.csv
    - LLBS_EW_landscape.csv
    - OV7_EW_landscape.csv
    - WHA_EW_landscape.csv
    - WHB_EW_landscape.csv
  - Each file includes:
    - Date, Field, Transect, Distance, Hedge/Margin indicator, Depth (Mustard/Topsoil), Sample type (A = abundance/count, B = biomass), plus species-level data
    - Species codes and names for endogeic, epigeic, and anecic earthworms (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)
    - Information on damaged or immature specimens (END/dm, EPI/dm, ANE/dm, etc.)
  - Landscape 2016 soil data file:
    - Landscape2016_soil_data.csv with 14 columns including Date, Field name, Code, Distance from hedge, multiple moisture readings (5 cm and 10 cm depths), soil temperatures (5 cm and 10 cm), and bulk density (5 cm and 15 cm)
  - Miscellaneous data: earthworm functional groups noted (Endogeic, Epigeic, Anecic) and their corresponding species

- Variables, units, and data coding
  - Earthworm counts and biomass (grams)
  - Distance from hedge (metres)
  - Hedge (H) vs Margin (M) sample designation
  - Depth indicators for sample type (Mustard pit vs Topsoil)
  - Species and functional group classifications for ecological interpretation

- Species and functional groups
  - Endogeic, Epigeic, and Anecic earthworm categories with multiple genus/species mappings
  - Functionality notes included (e.g., Endogeic damaged, Epigeic immature)

- References
  - Earthworms by Sims & Gerard (1999)

- Relevance for monitoring frameworks
  - Provides a structured, multi-site approach to monitoring soil biota (earthworms) as indicators of soil health and management impacts.
  - Defines standardized field protocols, measurement variables, and a comprehensive data schema enabling consistent aggregation, quality checks, and cross-site comparisons.
  - Includes explicit metadata around sample origin (hedge vs margin), depth, and transect geometry, supporting transparent data governance and traceability for environmental health assessments.
# Summary Experimental Design/Sampling Regime

- Purpose and scope
  - Documents earthworm sampling and soil measurements across multiple fields with different land uses, around hedges and field margins.
  - Data intended to support understanding of earthworm communities and soil properties in relation to landscape features and management.

- Experimental design
  - Sites and regimes: Little Langton (LL), Hutton Wandesley (HW), Overton (OV), Whenby (WH); transects per site = 1.
  - Land uses: LL with organic arable (A1) and organic arable (A2) and organic ley (B1/B2); HW with conventional ley and conventional arable; WH with organic ley and organic arable; LL includes paired transects for comparison.
  - Sampling dates: LL on 12- May-16 (A1/A2) and 13- May-16 (B1/B2); HW on 17- May-16; OV on 19- May-16; WH on 26- May-16.
  - Sample identifiers: LL A1, LL A2, LL B1, LL B2, HW A1/HWB, OV7, WHA/WHB, etc.
  - Sampling focus: earthworms by transect from hedge into field; hedge condition used as a reference; margins, 2 m increments, and specific depths.

- Field methods and instrumentation
  - Transect layout: 90 degrees from the hedge into the field; transects located mid-field where possible; paired transects for comparatives.
  - Soil pits: 18 x 18 x 15 cm, located at hedge, margin, and 2/4/8/16/32/64 m along transect.
  - Earthworm collection: hand-sorted soil, mustard solution extraction, ethanol preservation; identification using Sims and Gerard field key.
  - Additional measurements at pits: soil moisture (three readings in mV) at 5 and 10 cm depth (ML3 ThetaProbe); soil temperature at 5 and 10 cm (Checktemp1); soil bulk density at 5 and 15 cm using density rings; calculations on oven-dry basis.
  - Depths and coding: samples labeled as Hedge (H) or Margin (M); Mustard (P) vs Topsoil (S) depth indicators.

- Data collected and units
  - Primary earthworm data: number of earthworms; biomass in grams.
  - Spatial data: distance from hedge in metres.
  - Depth indicators: H (below hedge) or M (field margin); Depth codes include P (Mustard) and S (Topsoil).
  - Data types: Abundance/count (A) or Biomass (B) per sample.

- Data structure and files
  - Landscape data files (30-column CSVs): HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv.
  - Key columns: Date, Field, Transect, Distance, Hedge/Margin, Depth (Mustard or Topsoil), Sample type (A for abundance, B for biomass), followed by species-specific counts/biomass.
  - 30 species-related columns with codes and corresponding species names (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.) and functional groups (Endogeic, Epigeic, Anecic) plus damaged/immature categories.
  - Landscape dataset (Landscape2016_soil_data.csv): 14 columns including Date, Field name, code, distance from hedge, moisture at 5 cm and 10 cm (in millivolts), soil temperature at 5 cm and 10 cm, soil bulk density at 5 cm and 15 cm, etc.
  - Miscellaneous: Earthworm functional groups defined (Endogeic, Epigeic, Anecic) and mapping of codes to functional groups; blank cells indicate no data for some samples.

- Data quality, provenance, and metadata
  - Detailed metadata embedded in file headers and column definitions; explicit field codes for hedge (H) and margin (M) and depth indicators.
  - Explicit instrument models and measurement procedures for reproducibility.
  - Potential data gaps indicated by blank cells; standardized naming and file organization to support interoperability.
  - Reference framework for species identification: Sims and Gerard (1999).

- Coding, taxonomy, and references
  - Species codes mapped to widely used taxonomic names; functional grouping aids ecological interpretation.
  - Referenced taxonomic framework for earthworms: Sims & Gerard (1999).
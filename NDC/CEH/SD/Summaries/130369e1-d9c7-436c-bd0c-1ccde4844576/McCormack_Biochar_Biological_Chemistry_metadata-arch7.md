# Dataset schema for mesocosm experiment with biochar and soil properties

- Purpose and scope
  - Structured data describing a fully-factorial mesocosm experiment incorporating biochar treatment, crop types, and soil textures.
  - Designed to support map-based data products and spatial analyses of ecological and soil-chemistry variables.

- Key identifiers and treatments
  - Pot_Number: Unique identifier for each mesocosm
  - Biochar: Presence or absence of 2% biochar (w/w) in soil
  - Crop_Type: Barley (Hordeum vulgare L.), Ryegrass (Lolium perenne), or Unvegetated
  - Soil_Texture: SC (sandy clay), SZL (sandy silt loam), or CL (clay loam)
  - Year: Year of sampling
  - Block: Spatial block within the enclosure (one replicate per treatment per block in four blocks)

- Biological and chemical measurements
  - Density_Nematoda: Individuals per gram dry soil, from top 10 cm
  - Density_Microarthropod: Individuals per gram dry soil, from top 10 cm
  - Density_Collembola: Individuals per gram dry soil, from top 10 cm
  - Density_Acari: Individuals per gram dry soil, from top 10 cm
  - Aboveground_Biomass: Grams of aboveground plant biomass per mesocosm
  - Belowground_Biomass: Grams of belowground plant biomass per g-1 soil
  - Total_PLFA: nmol phospholipid fatty acid per g-1 soil
  - Bacterial_PLFA: nmol bacterial PLFA (specific fatty acids listed)
  - Fungal_PLFA: nmol fungal PLFA (specific fatty acids listed)
  - AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA (specific fatty acids listed)

- Soil chemical properties
  - soil_C: Soil carbon content (%)
  - soil_N: Soil nitrogen content (%)
  - non_py_soil_c: Adjusted soil carbon accounting for pyrogenic carbon by subtracting biochar carbon using specified equation
  - soil_moisture: Soil moisture (% by weight, via oven-drying protocol)
  - Soil_pH: Soil pH (measured from suspension with deionised water)

- Sampling, methods, and data notes
  - Sample depth: Top 10 cm of soil; core diameter ~3.5 cm; depth to 10 cm
  - Subsampling and analysis: 30 mg subsample used for carbon/nitrogen; carbon and nitrogen via flash combustion
  - Data representation: '.' indicates no sample taken
  - Special calculation: non_py_soil_c uses biochar carbon content (72.3%) and dose rate (2%) to adjust Ct to Ca with Ca = Ct − 0.02 × Cb / 0.98

- Data structure and integration considerations for GIS
  - Each row represents a mesocosm and sampling year; fields support spatial mapping via Pot_Number and Block
  - Units to be standardized for map visualizations:
    - Densities: individuals per gram dry soil
    - Biomass: grams per mesocosm
    - PLFA metrics: nmol g-1 soil
    - C, N: percent
    - Moisture: percent
    - pH: unitless (logically a pH value)
  - Missing data handling: account for '.' entries when creating spatial layers or aggregations
  - Potential map layers: mesocosm points or polygons colored by treatment, densities, PLFA groups, biomass, and soil properties; block-level spatial patterns can be examined separately or within the same map

- Practical GIS applications
  - Visualize spatial patterns of biota densities (nematodes, microarthropods, collembola, acari) and PLFA signals across treatments
  - Compare above- and belowground biomass alongside soil carbon/nitrogen and soil moisture pH
  - Assess the influence of biochar presence, crop type, and soil texture on soil microbial communities and chemical properties
  - Integrate with other spatial datasets (e.g., enclosure maps) for context and reporting

- Important caveats for analysts
  - Data come from multiple sources and spatial blocks; ensure consistent joining via Pot_Number and Block
  - Be mindful of potential data gaps indicated by '.' and apply appropriate imputation or exclusion in analyses
  - Ensure proper handling of the non_py_soil_c adjustment when calculating soil carbon-related metrics
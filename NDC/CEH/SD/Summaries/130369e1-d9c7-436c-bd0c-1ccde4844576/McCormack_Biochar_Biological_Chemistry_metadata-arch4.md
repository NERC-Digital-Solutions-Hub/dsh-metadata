# Pot_Number Unique identifier for each individual mesocosm

## Dataset Overview
- A fully described mesocosm dataset capturing biotic and abiotic responses to biochar, cropping, and soil texture treatments across multiple blocks and years.
- Includes plant, soil fauna, and microbial indicators along with soil chemical properties and basic physical measurements.
- Data notes indicate when samples were not taken (represented by a period).

## Variables and Measurements
- Treatments and identifiers
  - Biochar: Presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence
  - Crop_Type: Barley seeded at 1.8 t ha-1, Ryegrass seeded at 2.0 t ha-1, or Unvegetated
  - Soil_Texture: SC (sandy clay), SZL (sandy silt loam) or CL (clay loam)
  - Year: Year of sampling
  - Block: Spatial block within the enclosure; in a fully-factorial design, one replicate of each treatment combination per block
- Biotic density and biomass
  - Density_Nematoda: Individuals per gram dry soil from top 10 cm
  - Density_Microarthropod: Individuals per gram dry soil from top 10 cm
  - Density_Collembola: Individuals per gram dry soil from top 10 cm
  - Density_Acari: Individuals per gram dry soil from top 10 cm
  - Aboveground_Biomass: Grams of aboveground plant biomass per mesocosm, destructively harvested annually
  - Belowground_Biomass: Grams of belowground plant biomass per gram-1 soil
- Microbial phospholipid fatty acids (PLFA)
  - Total_PLFA: nmol phospho-lipid fatty acid g-1 soil
  - Bacterial_PLFA: nmol bacterial PLFA g-1 soil (e.g., i15:0, a15:0, etc.)
  - Fungal_PLFA: nmol fungal PLFA g-1 soil (e.g., 18:2?6,9)
  - AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA g-1 soil (e.g., 16:1?5)
- Soil chemical and physical properties
  - soil_C: Soil nitrogen content (%)  (Note: described as nitrogen content in the dataset)
  - soil_N: Soil carbon content (%)  (Note: described as carbon content in the dataset)
  - non_py_soil_c: Preexisting (non-pyrogenic) soil carbon; adjusted Ct to Ca using a specified equation and biochar carbon content
  - soil_moisture: Soil moisture calculated from weight loss upon oven drying
  - Soil pH: pH measured in a soil-water suspension
- Sampling details and procedures
  - Sampling depth: Top 10 cm of soil
  - Core size: 3.5 cm diameter to 10 cm depth
  - Subsampling for chemical analyses: 30 mg subsample from dried soil (105 °C ± 5, 24 h) for total carbon and nitrogen content via flash combustion
- Data handling notes
  - "." indicates no sample taken for that variable in a given mesocosm

## Data Processing and Adjustments
- non_py_soil_c adjustment: Ca = Ct - 0.02*Cb/0.98, where Ct is total measured % C in biochar-treated soil, Cb is biochar C content (72.3%), and the 0.02 represents a 2% dose.

## Data Quality and Metadata Considerations
- Sampling methodology explicitly described (depth, core size, drying and analysis methods) to support reproducibility and comparability.
- Clear notation for missing data (periods) to indicate absent samples.

## Implications for Data Strategy and Stewardship
- Rich, multi-dimensional dataset suitable for evaluating biochar effects on soil biota, microbial communities, and soil chemistry across crop treatments and soil textures.
- Well-defined units and measurement methods facilitate cross-study comparability and meta-analyses.
- The dataset embodies a comprehensive metadata framework (treatment details, sampling design, measurement techniques) that supports data discoverability, re-use, and collaboration across partners and disciplines.
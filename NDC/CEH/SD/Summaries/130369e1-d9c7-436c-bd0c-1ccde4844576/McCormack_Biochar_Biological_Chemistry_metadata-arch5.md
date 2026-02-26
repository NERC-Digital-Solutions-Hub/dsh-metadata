# Mesocosm Experiment Data Dictionary

## Overview
- Defines the dataset variables for a fully-factorial mesocosm experiment examining biochar presence, crop/type, soil texture, and environmental blocks.
- Captures biological, chemical, and physical measurements across replicates and time (Year of sampling).
- Includes detailed measurement methods and units for each variable, facilitating data sharing, discovery, and reuse.

## Key variables and measurements
- Pot_Number: unique identifier for each individual mesocosm.
- Biochar: presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence.
- Crop_Type: treatment category—Barley (Hordeum vulgare L.) at 1.8 t ha-1, Ryegrass (Lolium perenne) at 2.0 t ha-1, or Unvegetated.
- Soil_Texture: texture treatment—SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Year: year of sampling.
- Block: spatial block within the enclosure; in a fully-factorial design, one replicate of each treatment combination per block (four blocks total).
- Density_Nematoda: individuals per gram dry soil in the top 10 cm.
- Density_Microarthropod: individuals per gram dry soil in the top 10 cm.
- Density_Collembola: individuals per gram dry soil in the top 10 cm.
- Density_Acari: individuals per gram dry soil in the mesocosm.
- Aboveground_Biomass: grams of aboveground plant biomass per mesocosm, destructively harvested annually.
- Belowground_Biomass: grams of belowground biomass per g-1 soil.
- Total_PLFA: nmol phospho-lipid fatty acids per g-1 soil.
- Bacterial_PLFA: nmol bacterial PLFA (specific markers listed).
- Fungal_PLFA: nmol fungal PLFA (specific markers listed).
- AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA (specific markers listed).
- soil_C: soil nitrogen content expressed as a percentage (note: likely total carbon; see soil_N for carbon content).
- soil_N: soil carbon content expressed as a percentage (measured via flash combustion; see note for method).
- non_py_soil_c: preexisting non-pyrogenic soil carbon adjusted by subtracting soil carbon added via biochar using Eq. 1: Ca = Ct - 0.02*Cb/0.98 (Ca = adjusted C content; Ct = total measured % C in biochar-treated soil; Cb = C content of pure biochar, 72.3%; dose rate 2%).
- soil_moisture: soil moisture calculated from weight difference before and after oven drying (105 °C ± 5, 24 h).
- Soil pH: pH measured from a 1 g dried, milled soil subsample with 2 ml deionised water, using a calibrated pH probe after mixing and settling.
- note: '.' indicates no sample taken.

## Experimental design and data collection details
- Fully-factorial experiment with four spatial blocks, ensuring replication across treatment combinations.
- Sampling depth for density metrics is the top 10 cm; core diameter approximately 3.5 cm (3.5 cm Ø) to 10 cm depth.
- Destructive aboveground biomass measurements occur annually.
- PLFA measurements provide microbial community structure data (bacteria, fungi, and AM fungi) per gram of soil.
- Soil chemistry includes total carbon and nitrogen content with explicit preparation and instrumental methods.

## Data processing, provenance, and sharing
- Metadata includes explicit measurement methods, units, and key processing steps (e.g., non_py_soil_c adjustment).
- Derived fields (e.g., non_py_soil_c) are documented with the formula for reproducibility.
- Sample absence is indicated with a dot ('.'), enabling clear handling of missing data.
- Data should be uploaded to relevant portals and catalogued with standardized terminology and units to facilitate discovery and reuse.
- Documentation supports data quality assurance (QA) and cleaning prior to sharing, with potential for updates while respecting sharing limitations and provenance.
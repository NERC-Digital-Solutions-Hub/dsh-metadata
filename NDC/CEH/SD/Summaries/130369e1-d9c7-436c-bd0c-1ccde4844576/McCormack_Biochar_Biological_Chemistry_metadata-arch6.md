# Pot_Number Unique identifier for each individual mesocosm Biochar "Presence of 2 % biochar (w/w) in soil; + indicates presence, - indicates absence"

## Overview
- Dataset from a fully-factorial mesocosm experiment examining the presence of biochar (2% w/w) and its interaction with crop type and soil texture.
- Captures a wide range of biological, chemical, and physical soil measurements alongside plant biomass.
- Aims to support understanding of how biochar and other factors influence soil biota, microbial communities, and plant productivity.

## Treatments and Experimental Design
- Biochar treatment: presence vs. absence, indicated by + or -.
- Crop_Type: Barley (Hordeum vulgare L.) seeded at 1.8 t ha-1, Ryegrass (Lolium perenne) seeded at 2.0 t ha-1, or Unvegetated.
- Soil_Texture: SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Year: year of sampling.
- Block: one replicate per treatment combination across four spatial blocks in the fully-factorial setup.
- Design goal: enable comparisons across treatments and blocks to identify significant patterns.

## Variables and Measurements
- Density_Nematoda, Density_Microarthropod, Density_Collembola, Density_Acari: individuals per gram of dry soil from the top 10 cm.
- Aboveground_Biomass: grams of aboveground plant biomass per mesocosm, destructively harvested annually.
- Belowground_Biomass: grams of belowground plant biomass per gram of soil.
- Total_PLFA: nmol phospholipid fatty acids per gram of soil.
- Bacterial_PLFA: nmol of bacterial PLFA (specified fatty acids: i15:0, a15:0, 15:0, i16:0, 16:1?7, a17:0, i17:0, cy17:0, cis18:1?7, cy19:0).
- Fungal_PLFA: nmol fungal PLFA (18:2?6,9).
- AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA (16:1?5).
- soil_C: Soil carbon content (%). Measured via flash combustion on a 30 mg subsample.
- soil_N: Soil nitrogen content (%). Measured via flash combustion on a 30 mg subsample.
- non_py_soil_c: Adjusted soil carbon excluding biochar-derived carbon. Ca = Ct - 0.02*Cb/0.98, with Cb = 72.3% and dose rate 2%.
- soil_moisture: Soil moisture by weight difference before and after oven-drying (105 °C, ~24 h).
- Soil pH: Measured on a suspension of 1 g dried soil with 2 ml deionised water after shaking.

## Data Processing and Notation
- Note: '.' indicates that no sample was taken for that variable in a given instance.
- Derived/adjusted variable: non_py_soil_c uses a specific correction to remove biochar carbon contribution from total carbon measurements.

## Practical Implications for Data Use
- The dataset enables exploration of how biochar presence, crop type, and soil texture influence soil biota densities, microbial community composition via PLFA, and plant biomass production.
- Missing data are explicitly indicated, enabling careful handling in analyses.
- The combination of biological, chemical, and physical measurements supports multi-factor analyses and self-service data exploration through dashboards or reports.
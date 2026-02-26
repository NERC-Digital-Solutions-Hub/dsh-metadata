# Pot_Number Unique identifier for each individual mesocosm

## Overview
- Dataset from a fully-factorial mesocosm experiment examining the presence of 2% biochar in soil, crop treatment (Barley, Ryegrass, or Unvegetated), and soil texture (SC, SZL, CL).
- Includes multiple sampling years and four spatial blocks.
- Variables cover biotic densities (nematodes, microarthropods, Collembola, Acari), plant biomass (above and below), soil microbial/community indicators (PLFA profiles), and soil chemistry (carbon, nitrogen, moisture, pH).
- Each record corresponds to an individual mesocosm with a unique Pot_Number and associated treatment and measurement details.
- Note: '.' indicates that no sample was taken for that measurement.

## Experimental design and treatments
- Biochar: Presence of 2% biochar (w/w) in soil; coded as present or absent.
- Crop_Type: Barley (Hordeum vulgare L.), Ryegrass (Lolium perenne), or Unvegetated.
- Soil_Texture: SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Year: Year of sampling.
- Block: Spatial block within the enclosure (four blocks in the fully-factorial design).
- Replication: In each fully-factorial combination, one replicate per block.

## Variables and measurements
- Pot_Number: Unique identifier for each mesocosm.
- Biochar: Presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence.
- Crop_Type: Barley, Ryegrass, or Unvegetated.
- Soil_Texture: SC, SZL, or CL.
- Year: Year of sampling.
- Block: Spatial block of mesocosm within the enclosure.
- Density_Nematoda: Individuals per gram dry soil sampled from top 10 cm of each mesocosm.
- Density_Microarthropod: Individuals per gram dry soil sampled from top 10 cm of each mesocosm.
- Density_Collembola: Individuals per gram dry soil sampled from top 10 cm of each mesocosm.
- Density_Acari: Individuals per gram dry soil sampled from top 10 cm of each mesocosm.
- Aboveground_Biomass: Grams of aboveground plant biomass per mesocosm.
- Belowground_Biomass: Grams of belowground plant biomass per g-1 soil.
- Total_PLFA: nmol phospho-lipid fatty acid per g-1 soil.
- Bacterial_PLFA: nmol bacterial phospho-lipid fatty acid g-1 soil (specific markers listed).
- Fungal_PLFA: nmol fungal phospho-lipid fatty acid g-1 soil (specific markers listed).
- AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA g-1 soil.
- soil_C: Soil nitrogen content (%).
- soil_N: Soil carbon content (%).
- non_py_soil_c: Preexisting (non-pyrogenic) soil carbon; adjusted Ct to Ca with Eq. 1: Ca = Ct - 0.02*Cb/0.98, where Cb is biochar carbon content (72.3%) and 0.02 is the dose rate.
- soil_moisture: Soil moisture (% by weight) calculated from pre- and post-drying weights.
- Soil pH: pH measured from a 1 g soil subsample with 2 ml deionised water, shaken, settled, and measured with a pH probe.
- note: '.' = 'period' indicates no sample taken.

## Measurement methods
- Carbon and nitrogen: Total C and N by flash combustion at 950 °C using an elemental analyser (EL Cube).
- Soil moisture: Oven drying at 105 °C ± 5 for 24 h with weight change used to determine moisture.
- Soil pH: Prepared from dried soil slurry (1 g soil, 2 ml water) with shaking and measurement using a pH probe.
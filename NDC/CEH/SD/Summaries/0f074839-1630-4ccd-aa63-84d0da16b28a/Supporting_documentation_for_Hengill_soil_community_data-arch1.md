# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- Dataset from 96 soil habitat patches in the Hengill geothermal valley, Iceland, collected in July 2013.
- Covers environmental variables (soil temperature, moisture, pH, total carbon, total nitrogen), vegetation cover (non-plant groups and plant species), and invertebrate communities (abundance and mean dry body mass).
- Patches span a natural soil temperature gradient of 7–38 °C, with patches close together and similar soil moisture, pH, carbon, and nitrogen.
- Sampling across 16 geothermally heated streams (3 patches per bank) to study effects of temperature on plant and invertebrate communities; links to broader warming studies.

## Sampling regime and collection methods
- Soil temperature: iButton DS1921G loggers buried 10 cm below the surface; measurements every 10 minutes over 48 hours at each patch.
- Soil moisture: measured with a TRIME-TDR probe at each patch.
- Soil chemistry: five 1.5 × 5 cm cores collected per patch; soil dried at 60 °C for 96 hours and milled for analysis; soil pH measured from 10 g of dry soil (1:5 soil-to-water); total carbon and total nitrogen measured with a CN analyser.
- Vegetation survey: 0.5 × 0.5 m quadrats placed randomly; photographs taken and analyzed by cover class to estimate percentage cover; plants identified to species level (except graminoids); recorded cover for grasses, mosses, lichens, and litter.
- Invertebrate sampling: five pitfall traps per patch arranged to cover a 1 m² area (four corners and center); traps filled with ethylene glycol and stream water; left for 48 hours; samples combined, stored in 70% ethanol; individuals identified to species where possible with microscopy.
- Data collection details and procedures referenced to Robinson et al. (2018) and related publications.

## Data structure and files
- Data provided in four comma-separated value files; each row corresponds to one of the 96 habitat patches.
- Common first three columns across files:
  - Column 1: stream (identifier linked to previous Hengill publications)
  - Column 2: bank (left or right bank at a stream confluence)
  - Column 3: habitat patch (1–3; patch proximity to the river)
- hengill_environmental_data.csv
  - Columns 4–5: latitude and longitude (decimal GPS coordinates)
  - Column 6: temperature (mean soil temperature in °C)
  - Columns 7–8: total_carbon and total_nitrogen (g kg⁻¹)
  - Columns 9–10: moisture (%) and pH
- hengill_vegetation_cover.csv
  - Columns 4–38: names of non-plant groups (grasses, mosses, lichens, litter) and plant species quantified
  - Data in columns 4–38 are percentage cover
- hengill_invertebrate_abundance.csv and hengill_invertebrate_mass.csv
  - Columns 4–82: names of invertebrate species quantified
  - Environmental file structure mirrors these two files in terms of column count
  - hengill_invertebrate_abundance.csv: number of individuals per habitat patch
  - hengill_invertebrate_mass.csv: mean dry weight of each species (in milligrams)

## Variables and interpretation
- Environmental data: site-level soil temperature, moisture, pH, carbon, and nitrogen to assess abiotic context for biotic communities.
- Vegetation data: percent cover of non-plant groups and detailed plant species cover to examine plant community structure across the temperature gradient.
- Invertebrate data: species-level abundance and mean body mass to analyze how consumer communities respond to environmental gradients and vegetation structure.
- All patch-level data enable analysis of relationships between temperature, soil properties, plant communities, and invertebrate communities.

## References and context
- Data linked to numerous studies on temperature effects, community structure, and ecological warming (examples include Robinson et al. 2018; O’Gorman et al. 2012, 2016, 2017; Friberg et al.; Woodward et al.; Adams et al.; Demars et al.; others).
- The dataset supports investigations into how natural warming gradients influence structure and function of aquatic and terrestrial habitats, particularly in geothermal systems.
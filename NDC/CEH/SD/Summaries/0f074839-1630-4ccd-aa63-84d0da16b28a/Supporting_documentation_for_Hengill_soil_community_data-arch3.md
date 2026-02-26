# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland

- Aim and scope
  - A dataset of environmental variables (soil temperature, moisture, pH, total carbon, total nitrogen) plus biological measures (aboveground vegetation cover, total invertebrate abundance, and mean invertebrate body mass) collected across 96 soil habitat patches in the Hengill geothermal valley, Iceland, in July 2013.
  - Patches span a soil temperature gradient (7–38°C) within a compact area (~2 km) with similar moisture, pH, carbon, and nitrogen.
  - Data are intended to support analyses of how soil temperature and associated environmental factors shape plant and invertebrate communities; linked to prior and ongoing ecology studies in the region (e.g., Robinson et al. 2018).

- Sampling regime and collection methods
  - Soil temperature: 10 cm below the surface via iButton loggers; readings every 10 minutes over 48 hours.
  - Soil moisture: measured with Imko TRIME-TDR probes.
  - Soil cores: five cores per patch (1.5 × 5 cm), homogenised, dried at 60°C for 96 hours, milled for analysis.
  - Soil pH: measured on 10 g of dry milled soil with a 1:5 soil-to-water ratio using a pH meter.
  - Total carbon and total nitrogen: measured by combustion using a CN analyser (Carlo Erba Flash 1112).
  - Vegetation survey: 0.5 × 0.5 m quadrats per patch; random placement; photographed; cover classes used to describe species abundance; vascular plants identified to species; grasses, mosses, lichens, and litter noted separately.
  - Aboveground invertebrates: five pitfall traps per patch (corner and center within a 1 m^2 area); traps filled with ethylene glycol and water; left for 48 hours; samples combined, sieved, and preserved in 70% ethanol; identification to species where possible with microscopy.

- Data structure
  - Data are provided in four CSV files; each row corresponds to one of the 96 habitat patches.
  - Common first three columns in all files: (1) stream, (2) bank, (3) patch (1–3) within the stream segment.
  - hengill_environmental_data.csv
    - Columns 4–5: latitude and longitude (decimal GPS coordinates).
    - Column 6: mean soil temperature (°C).
    - Columns 7–8: total carbon (g kg−1) and total nitrogen (g kg−1).
    - Columns 9–10: soil moisture (%) and pH.
  - hengill_vegetation_cover.csv
    - Columns 4–38: names of non-plant groups (grasses, mosses, lichens, litter) and plant species; data are percentage cover.
  - hengill_invertebrate_abundance.csv and hengill_invertebrate_mass.csv
    - Columns 4–82: names of invertebrate species.
    - In abundance.csv: counts per habitat patch.
    - In mass.csv: mean dry weight per species (milligrams).

- Relevance for monitoring frameworks and policy
  - Demonstrates integration of environmental conditions with multiple biological indicators across a fine spatial scale and a defined gradient, enabling monitoring of ecosystem response to temperature and related factors.
  - Provides concrete measures aligned with environmental health monitoring: abiotic (temperature, moisture, pH, C, N) and biotic (vegetation cover by species/groups; invertebrate community structure and body mass).
  - Data are structured for comparability across patches and over time (with precise metadata on location and methods), aiding governance, data sharing, and transparency in monitoring outputs.

- Data quality, metadata, and governance considerations
  - Rich metadata including sampling methods, spatial coordinates, and clear file structures support data provenance and reproducibility.
  - Methodological detail facilitates standardization and potential integration with other monitoring datasets.
  - Considerations for data governance in monitoring contexts: openness of underlying data, data-sharing agreements, versioning, and ensuring consistency in units and taxonomic resolution when integrating with other datasets.

- References and context
  - Associated with multiple studies on warming effects and ecological structure in geothermal streams (e.g., Robinson et al. 2018; several related works cited in the dataset).
# Impact of grassland management on biomass production and nutritional quality, invertebrate communities, and soil health, from an experimental site in Berkshire, UK.

- Overview
  - Describes a field-scale, multi-factorial experiment (2009–2012) in Berkshire, UK, funded by Defra (BD1466), assessing how seed mix, management type and intensity, and cultivation techniques affect grassland production, nutrition, pollinators, predatory beetles, and soil health.
  - Aims to inform how different plant functional groups and management practices deliver ecosystem services.

- Data assets (four CSV files) and contents
  - rawdata_biomass production and quality.csv
    - Measures: dry matter yield and herbage nitrogen content
    - Plot-level data across 48 plots (for cutting treatments) over 2009–2012
    - Key fields: Plot, Seed, Management, Intensity, Cultivation, Block, Year, quality_herbage_n, production_dry_yield
  - rawdata_invertebrates.csv
    - Measures: pollinator abundance and species richness; predatory beetle abundance, species richness, and biomass
    - Data across 96 plots over 2009–2012
    - Key fields: Plot, Seed, Management, Intensity, Cultivation, Block, Year, pollinator_abundance, pollinator_species_richness, predatory_beetle_abundance, predatory_beetle_mass, predatory_beetle_species_richness
  - rawdata_soil_bulkdensity.csv
    - Measures: soil bulk density (0–10 cm horizon)
    - Data from plots under intensive/intensive treatments across years 2009, 2010, 2012
    - Key fields: plot, seed, management, intensity, cultivation, block, year, bulk_density
  - rawdata_soil_nitrogen and carbon.csv
    - Measures: total soil nitrogen and total soil carbon
    - Data across 48 plots for multiple years
    - Key fields: plot, seed, management, intensity, cultivation, block, year, total_nitrogen, total_carbon
  - Metadata descriptions accompany each file, detailing column meanings and units.

- Study design and data collection
  - Experimental design: field-scale, multifactorial, randomised split-split-split-plot across four blocks
  - Four seed treatments at whole-plot level: Grass (G), Grass & Legume (GL), Grass, Legume & Forbs (GLF)
  - Management treatment: Grazing vs Cutting (silage to 10 cm)
  - Management intensity: Intensive vs Extensive
  - Cultivation treatment: Deep ploughing vs Minimum tillage
  - No inorganic fertilizer used during the experiment
  - Seed bed establishment and seed rates varied by seed treatment (seed composition detailed in Table 1)

- Measurements and methods
  - Biomass and quality: annual cutting, sampling, and oven-drying to determine dry matter yield; nitrogen content (%N) measured May each year
  - Pollinators: fixed transects (two 20 m x 2 m) surveyed 3 times per year for butterfly and bee species richness and abundance; standardized timing and weather considerations
  - Predatory beetles: Vortis suction sampling in June and September; specimens identified to species; biomass calculated from length-mass relationships
  - Soil health: soil bulk density measured 0–10 cm horizon (2009, 2010, 2012) using multiple cores; total soil nitrogen and carbon measured from selected cores
  - Quality control: trained surveyors and standardized data collection forms; data checked for anomalies

- Provenance, quality, and related work
  - Data collected under standardized protocols with field and lab forms; cross-year checks for anomalies
  - Related publications and supplemental papers:
    - Enhancing floral resources for pollinators in productive agricultural grasslands (Biological Conservation, 2014)
    - Enhancing beetle and spider communities in agricultural grasslands: the roles of seed addition and habitat management (Agriculture, Ecosystems & Environment, 2013)
  - Supplemental information provides full methods and context to support data interpretation and reuse

- Data governance, reuse potential, and limitations
  - Rich, multi-year, multi-response dataset suitable for cross-study meta-analyses on grassland management and ecosystem services
  - Enables examination of interactions among seed mix, management type/intensity, and cultivation on biomass, nutrition, pollinators, beetles, and soil health
  - Limitations: single-site Berkshire, UK; experimental conditions (no fertilizer) may limit generalizability to different ecosystems or management regimes; dataset covers 2009–2012 with four-year window
  - Governance and discovery considerations for Data Leaders:
    - clear multi-layer experimental design facilitates understanding of causal relationships and interaction effects
    - well-structured metadata and per-file data dictionaries support discoverability and interoperability
    - potential for integration with broader grassland data networks to support policy and practice across regions

- Key takeaways for data strategy
  - The dataset exemplifies a robust, multi-factor grassland experiment with comprehensive measurements across biological, chemical, and physical soil health indicators
  - Strong metadata and standardized protocols enhance data discoverability, reuse, and cross-study comparability
  - Useful for developing data products or dashboards that map seed mix and management practices to ecosystem services outcomes
  - Highlights the importance of documenting provenance, measurement methods, and experimental design to support credible reuse by policy colleagues and research partners
# Impact of grassland management on biomass production and nutritional quality, invertebrate communities, and soil health, from an experimental site in Berkshire, UK.

## Overview
- Describes a field-scale, multi-factorial experiment (2009–2012) in Berkshire, UK, examining how seed mix, management method, management intensity, and seed bed cultivation affect grassland productivity, nutritional quality, pollinator and predatory beetle communities, and soil health.
- No inorganic fertilizer was applied; designs test seed mixtures (grass only, grass with legume, grass with legume and forbs), management as grazing or cutting, intensity as intensive or extensive, and cultivation as deep ploughing or minimum tillage.

## Experimental design
- Location: Warfield, Berkshire; previously floristically poor sward dominated by Lolium perenne and Trifolium repens.
- Design: field-scale, multifactorial, randomized split-split-split-plot across four blocks; 24 treatment levels across 96 plots (approx. 875 m2 each).
- Seed mix treatments (whole-plot level):
  - G: grasses only
  - GL: grasses + legumes
  - GLF: grasses + legumes + forbs
- Management (split-plot): grazing vs cutting (silage to 10 cm)
- Intensity (split-split-plot): intensive vs extensive
- Cultivation (split-split-split plot): deep ploughing vs minimum tillage (non-inversion)
- Treatments were implemented across plots with detailed seed mix compositions and sowing rates; measurements taken over four years.

## Data files and key variables
- The dataset comprises four CSV files with accompanying metadata:
  - rawdata_biomass_production_and_quality.csv
    - Plot, Seed, Management, Intensity, Cultivation, Block, Year, quality_herbage_n (%N), production_dry_yield (dry matter yield)
  - rawdata_invertebrates.csv
    - Plot, Seed, Management, Intensity, Cultivation, Block, year, predatory_beetle_mass, predatory_beetle_abundance, predatory_beetle_species_richness, pollinator_abundance, pollinator_species_richness
  - rawdata_soil_bulkdensity.csv
    - Plot, Seed, Management, Intensity, Cultivation, Block, year, bulk_density
  - rawdata_soil_nitrogen_and_carbon.csv
    - Plot, Seed, Management, Intensity, Cultivation, Block, year, total_nitrogen, total_carbon
- Column concepts:
  - Plot and Block: plot identifiers and replicate blocks
  - Seed: seed treatment (G, GL, GLF)
  - Management: Cut or Graze
  - Intensity: Typical vs Rest; Intensive vs Extensive
  - Cultivation: Deep vs Shallow (minimum tillage)
  - Year: 2009–2012
  - Biodiversity measures: pollinators (abundance, species richness), predatory beetles (mass, abundance, species richness)
  - Soil measures: bulk density (0–10 cm), total nitrogen, total carbon
  - Biomass measures: dry matter yield; herbage nitrogen content (%N)

## Measurements and methods
- Biomass and quality: annual cutting (10 cm height), sample processing to determine dry matter yield and %N.
- Pollinators: two fixed 20 m x 2 m transects per plot; surveys in spring, midsummer, and late summer; taxa include butterflies, Apis mellifera, Bombus spp., solitary bees, hoverflies; species richness and total abundance calculated.
- Predatory beetles: Vortis suction sampling (June and September) across plots; approximately 55 suction samples per plot per year; beetles identified to species and categorized as predatory or phytophagous; biomass computed from length-mass relationships.
- Soils: bulk density measured in 0–10 cm horizon (2009, 2010, 2012) using replicated cores; total nitrogen and carbon measured from sub-samples of the same plots at the same years.

## Data quality and provenance
- Surveyors and lab personnel were trained; standardized protocols followed; field and lab data recorded with specific forms.
- Data checked for anomalous entries to ensure consistency across years and treatments.
- Supplemental information includes related scientific papers and formal metadata describing variable meanings and units.

## Supplemental information and related publications
- Related papers:
  - Enhancing floral resources for pollinators in productive agricultural grasslands (Biological Conservation, 2014)
  - Enhancing beetle and spider communities in agricultural grasslands: the roles of seed addition and habitat management (Agriculture, Ecosystems & Environment, 2013)
- Provisions for provenance and quality details are included in the metadata and methods sections of the dataset description.

## How to use and potential data products
- Suitable for cross-year comparisons of treatment effects on:
  - Biomass production and forage quality
  - Pollinator and predatory beetle communities
  - Soil health metrics (bulk density, nitrogen, carbon)
- Opportunities to create self-serve data products:
  - Dashboards comparing seed mix effects (G vs GL vs GLF) under different management and cultivation regimes
  - dashboards or pivot-style reports linking biodiversity indicators to biomass yield and soil health
  - integrated analyses across the four CSVs to explore relationships between soil properties, productivity, and invertebrate communities
- Considerations for integration:
  - Align plots by Block, Year, Seed, Management, Intensity, and Cultivation to build multi-plot comparisons
  - Use Year as a temporal axis to assess year-to-year variability and treatment consistency

## Notes for data reuse
- The dataset originates from a Defra-funded project (BD1466) and includes detailed methodological documentation and seed mix compositions (Table/figure references in the full description).
- No inorganic fertilizer was used, which is important when comparing to other fertilized grassland studies.
- Data are best used with awareness of the hierarchical experimental design (block, plot, seed/main-treatment, sub-treatments) to properly model treatment effects.
# Impact of grassland management on biomass production and nutritional quality, invertebrate communities, and soil health, from an experimental site in Berkshire, UK.

## Aim
- Describe how different grassland management techniques influence biomass production, nutritional quality, pollinator communities, predatory beetle communities, and soil health.

## Study overview
- Location: Warfield, Berkshire, UK (grid reference SU9073)
- Timeframe: 2009–2012
- Design: Field-scale, randomised, multifactorial, split-split-split-plot experiment
- Treatments replicated across four blocks; no inorganic fertilisers applied

## Treatments and experimental layout
- Seed mixtures (whole-plot level; SEED):
  - G: Grass only (five grass species)
  - GL: Grass + legume (five grasses + seven legumes)
  - GLF: Grass + legume + forbs (five grasses, seven legumes, six forbs)
- Seed bed cultivation (CULTIVATION):
  - Deep ploughing (herbicide + inversion tillage to 25–30 cm)
  - Minimum tillage (non-inversion, disturbance ~40% of area to ~5 cm)
- Management (MANAGEMENT; split over SEED):
  - Grazing (cattle at 3 LU ha−1)
  - Cutting for silage to 10 cm
- Management intensity (INTENSITY; split over MANAGEMENT):
  - Intensive (grazing May–October or two silage cuts)
  - Extensive (grazing with a mid-year rest or one silage cut)
- Experimental scale: 24 treatment levels across 96 plots (average plot size ~875 m2)

## Data collected and outputs
- Biomass production and nutritional quality (Yearly, 2009–2012):
  - Dry matter yield (biomass)
  - Herbage nitrogen content (%N)
- Invertebrate communities (Yearly, 2009–2012):
  - Pollinators: abundance and species richness
  - Predatory beetles (Carabidae and Staphylinidae): abundance, species richness, biomass
- Soil health (Years 2009, 2010, 2012):
  - Bulk density (0–10 cm)
  - Total soil nitrogen (%N) and total soil carbon (%C)

## Data collection methods
- Biomass:
  - Post-cut sample from a 5 m strip per plot; 0.5 kg sample dried at 80°C to determine dry matter yield
  - May cut nitrogen content measured on first cut
- Pollinators:
  - Two fixed 20 m × 2 m transects per plot; surveys in three periods per year (pre-cut, post-first cut, pre-final cut)
  - Identification to species level for butterflies; Apis mellifera; Bombus spp. to specified taxa; solitary bees; hoverflies
- Predatory beetles:
  - Vortis suction sampler; June and September; 55 suction replicates per plot
  - Species-level identification; classified as predatory or phytophagous
  - Biomass derived from length–mass relationships
- Soil:
  - Bulk density: 0–10 cm horizon, 5 cores per plot in 2009, 2010, 2012
  - Total N and total C: additional cores from same plots in October 2009, 2010, 2012

## Data files and structure
- Four CSV files with accompanying metadata:
  - rawdata_biomass_production_and_quality.csv
    - Includes: Plot, Seed, Management, Intensity, Cultivation, Block, Year, production_dry_yield, quality_herbage_n
  - rawdata_invertebrates.csv
    - Includes: Plot, Seed, Management, Intensity, Cultivation, Block, year, predatory_beetle_mass, predatory_beetle_abundance, predatory_beetle_species_richness, pollinator_abundance, pollinator_species_richness
  - rawdata_soil_bulkdensity.csv
    - Includes: plot, seed, management, intensity, cultivation, block, year, bulk_density
  - rawdata_soil_nitrogen_and_carbon.csv
    - Includes: plot, seed, management, intensity, cultivation, block, year, total_nitrogen, total_carbon
- Each file includes detailed column descriptions and units; metadata explains variable meanings and study design

## Provenance and quality
- Defra project BD1466; data collection followed standardised protocols; trained surveyors and lab personnel
- Data checked for anomalous entries; methods detailed to enable reproducibility
- Related publications provided for context and further analysis

## Potential uses for environmental monitoring
- Multi-mactor, time-series dataset enabling assessment of management impacts on productivity, quality, biodiversity, and soil health
- Standardised framework suitable for integration with other land-management datasets to evaluate policy performance
- Opportunities to enhance data value by combining with external datasets and enabling broader data access and reuse
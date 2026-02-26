# Impact of grassland management on biomass production and nutritional quality, invertebrate communities, and soil health, from an experimental site in Berkshire, UK.

- An experimental dataset describing how different management techniques affect grassland biomass production (dry matter yield), nutritional quality (herbage nitrogen content), pollinator communities, predatory beetle communities, and soil health (bulk density, total soil carbon and nitrogen).
- Location and duration: Warfield, Berkshire, UK; field-scale, randomised block experiment conducted from 2009–2012; Defra-funded project (BD1466).
- Site characteristics: Floristically species-poor sward dominated by Lolium perenne and Trifolium repens at baseline; no inorganic fertilizer used during the experiment.

## Study design and site details

- Experimental framework: multifactorial field-scale design implemented in April 2008, with a randomised split-split-split-plot layout across four blocks.
- Treatment axes (four hierarchical levels):
  - Seed mix (whole-plot level): Grass only (G); Grass & legume (GL); Grass, legume & forbs (GLF).
  - Management (split-plot): Grazing vs cutting for silage.
  - Management intensity (split-split-plot): Intensive vs extensive.
  - Cultivation (split-split-split-plot): Deep ploughing vs minimum tillage.
- Plot scale and replication: 24 treatment levels across 96 plots; average plot size ~875 m2.
- Fertilization: None of the treatments received inorganic fertilizer.
- Seed mix composition and sowing rates: Detailed in the seed mix table (G, GL, GLF with grasses, legumes, and forbs; specific species and sowing rates provided).

## Treatments and data collection scope

- Seed bed establishment and cultivation: Autumn 2008; deep ploughing vs minimum tillage.
- Management practices: Cattle grazing (three livestock units ha-1) or silage cutting; intensity variations (intensive vs extensive).
- Measured outcomes across years (2009–2012):
  - Biomass production and nutritional quality: Dry matter yield and herbage nitrogen content (%N); measured from plots under cutting management.
  - Pollinator communities: Abundance and species richness for butterflies, honey bees, bumblebees, solitary bees, and hoverflies; standardized transects and survey timings.
  - Predatory beetle communities: Abundance, species richness, and biomass for Carabidae and Staphylinidae; collected via Vortis suction sampling.
  - Soil health: Soil bulk density (0–10 cm horizon) and total soil nitrogen (%N) and carbon (%C) from soil cores; targeted sampling years were 2009, 2010, and 2012.
- Sampling cadence and methods:
  - Biomass: Harvesting strips from plots, drying, and calculating dry matter yield; nitrogen via LECO method.
  - Pollinators: Three annual surveys per year along fixed 20 m x 2 m transects, conducted under suitable weather conditions, with taxonomic resolution down to species level for key groups.
  - Beetles: Suction sampling in June and September; 55 suction events per plot per year; beetles identified to species and categorized as predatory or phytophagous.
  - Soils: Core sampling for bulk density; deeper subsamples for total nitrogen and carbon analyses.

## Data files and structure

- Four CSV files composing the dataset:
  - rawdata_biomass_production_and_quality.csv
    - Variables: Plot, Seed, Management, Intensity, Cultivation, Block, Year, quality_herbage_n (%N), production_dry_yield (dry matter yield).
    - Notes: 48 plots with cutting management; measurements across 2009–2012.
  - rawdata_invertebrates.csv
    - Variables: Plot, Seed, Management, Intensity, Cultivation, Block, year, pollinator_abundance, pollinator_species_richness, predatory_beetle_abundance, predatory_beetle_mass, predatory_beetle_species_richness.
    - Notes: 96 plots across 2009–2012; includes pollinators and predatory beetles.
  - rawdata_soil_bulkdensity.csv
    - Variables: plot, seed, management, intensity, cultivation, block, year, bulk_density.
    - Notes: 0–10 cm horizon; 2009, 2010, 2012; intensive management subset.
  - rawdata_soil_nitrogen_and_carbon.csv
    - Variables: plot, seed, management, intensity, cultivation, block, year, total_nitrogen, total_carbon.
    - Notes: Measurements across 2009, 2010, 2012.
- Metadata and documentation:
  - Each file includes detailed column definitions and units.
  - Methods and references described in the methods section and supporting documentation.
  - Provenance: Standardized field and lab protocols; data checked for anomalies; trained surveyors and lab personnel.

## Methods and measurement specifics (for GIS data interpretation)

- Pollinators and beetles:
  - Taxonomic resolution includes species-level data for butterflies, Apis mellifera, Bombus spp., and selected hoverflies for pollinators; predatory beetles include Carabidae and Staphylinidae.
  - Abundance and species richness captured annually per plot; biomass of predatory beetles computed from length-mass relationships.
- Soils:
  - Bulk density measured at 0–10 cm via core method; nitrogen and carbon measured from sub-samples of soil cores.
  - Sampling years include 2009, 2010, 2012 (with intensive management plots enabling deeper soil property comparisons).
- Data quality:
  - Training, standardized forms, and protocol adherence across field and lab teams; data checks for anomalous entries.

## GIS-ready considerations and potential map products

- Spatial scope and location:
  - Study site located at grid reference SU9073, Warfield, Berkshire; plots arranged within four blocks under a hierarchical experiment layout.
- Possible GIS products:
  - Per-plot time-series maps of biomass yield and %N across years 2009–2012.
  - Spatial layers showing seed-mix treatments (G, GL, GLF) overlaid with management type (grazing vs cutting) and cultivation method (deep plough vs minimum tillage).
  - Multivariate maps integrating pollinator abundance/richness, predatory beetle metrics, and soil health indicators (bulk density, %N, %C) to explore spatial associations with management intensity.
  - Comparison layers for intensive vs extensive management and their influence on ecosystem services across the field.
- Data integration notes:
  - While plot coordinates are not explicitly provided in the summary metadata, plots are defined within a four-block experimental layout at a known Berkshire site; GIS work would map plots to accompanying spatial coordinates if available from the dataset’s supporting documentation.

## Provenance and related literature

- Related publications:
  - Woodcock et al. (2014) Enhancing floral resources for pollinators in productive agricultural grasslands.
  - Woodcock et al. (2013) Enhancing beetle and spider communities in agricultural grasslands: the roles of seed addition and habitat management.
- Data quality and stewardship:
  - Provisional and final data follow standardized ecological analysis references; training and standardized protocols employed; anomaly checks conducted.
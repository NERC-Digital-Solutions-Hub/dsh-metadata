# Measurements of microarthropod community structure and diversity from an upland grassland experimental site

- Overview
  - Data from the NERC Soil Biodiversity Programme at Sourhope, Scotland, focused on how microarthropod communities relate to soil fertility, productivity, and diversity.
  - Experimental design involved fertilization (nitrogen and lime) and monitoring of below- and above-ground factors over 1999–2000.
  - Outputs support map-based exploration of microarthropod abundance, diversity, and soil functional indicators.

- Site description and sampling design (spatial context)
  - Location: Sourhope, Cheviot Hills, south-east Scotland; semi-improved upland grassland at ~350 m altitude.
  - Coordinates: around 55°28'30"N, 2°14'W; grid reference NT8545019630.
  - Soil: humic brown (Sourhope series).
  - Experimental layout: five blocks downslope; each block has six plots (12 × 20 m) with random treatments.
  - Treatments: control, nitrogen (NH4NO3), lime (CaCO3), nitrogen + lime.
  - Sampling scheme: soil cores taken at four times (Nov 1999, Feb 2000, May 2000, Aug 2000); depths and core types varied by dataset.
  - Core handling: Berlese-Tullgren extraction for microarthropods; subsamples for root, soil chemistry, and microbial measurements.

- Data products (datasets)
  - Dataset 1040: Plant species data (P2133_FIELD_BOTANICAL_PERCENT.csv)
    - Spatial keys: SUID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y; sampling date; surface area; TREATMENT.
    - Content: plant species names and percent cover per sampling unit; used to relate vegetation to microarthropod communities.
  - Dataset 1041: Field microarthropod population density data (P2133_FIELD_MPOD_NUMBERS.csv)
    - Spatial/experimental keys as above; depth to 5 cm.
    - Content: counts of microarthropods (mites, Collembola) per core, expressed as numbers per m^2.
  - Dataset 1042: Field microarthropod species abundance data (P2133_FIELD_MPOD_SPECIES.csv)
    - Keys similar to 1041; depth to 5 cm.
    - Content: species-level counts per core for microarthropods.
  - Dataset 1043: Field soils data (P2133_FIELD_SOILS.csv)
    - Keys include SUID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, DEPTH_FROM/TO, TREATMENT, SURFACE_AREA, SAMPLE_TYPE.
    - Content: soil and root properties per core, including microbial biomass C (BIOMASSC), soil respiration, pH, loss on ignition (LOI), root and soil C/N ratios, percent moisture, dry root biomass, and depth measurements.

- Measurements and variables (GIS-ready considerations)
  - Microarthropods
    - Abundance: population density per core (1041); depth to 5 cm.
    - Species: abundance by species (1042); dominant taxa and identification notes.
    - Calculations: diversity indices for microarthropods (overall and group-specific: mites, Collembola).
    - Biomass: estimated microarthropod biomass per core using established conversion factors.
  - Soil and root chemistry
    - Soil moisture, pH (wet-measurement), organic matter (LOI), total carbon and nitrogen (soil and roots), microbial biomass carbon (fumigation-extraction), basal respiration (CO2).
    - Root biomass per core; dry mass measurements.
    - Depth ranges: from 0–5 cm for microarthropod and chemical measurements; occasionally 8 cm core depth for some root/soil analyses.
  - Plant data
    - Plant species composition and percent cover per core/unit; linked to microarthropod communities via SUID and plot-level treatments.
  - Data structure
    - Four CSV files with standardized fields: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, and specific measurement fields per dataset.

- Methods (key steps for GIS integration)
  - Sampling: five blocks, six plots per block; N and lime fertilization schemes; sampling times: Nov 1999, Feb 2000, May 2000, Aug 2000.
  - Microarthropod extraction: Berlese-Tullgren funnels (96 hours) from cores; species identification and counts.
  - Diversity and biomass metrics: Shannon-Wiener index, evenness, cumulative richness; biomass conversion factors applied to taxa.
  - Soil and root analyses: DNA-free standard methods for C, N; microbial biomass via fumigation-extraction; respiration via CO2 headspace measurement.
  - Quality control: numeric range checks, formatting checks, and logical integrity checks; data are QA’d but not guaranteed to be accurate or fit for all uses; liability disclaimer included.

- Practical GIS applications and considerations
  - Spatial visualization: map microarthropod density and diversity across blocks, plots, and cells; link to soil properties and plant data.
  - Multi-layer integration: combine 1041/1042 density and species data with 1043 soil properties and 1040 plant data for spatial analyses of biodiversity-function relationships.
  - Temporal dimension: incorporate sampling dates to show changes over time and treatment effects.
  - Data readiness: fields include explicit GIS-friendly keys (SUID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, DEPTH_FROM/TO, TREATMENT) to facilitate joins and spatial summarization.
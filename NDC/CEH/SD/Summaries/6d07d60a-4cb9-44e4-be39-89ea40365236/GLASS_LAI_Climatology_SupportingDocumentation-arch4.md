# Global gridded monthly mean Leaf Area Index (LAI) for five Plant Functional Types (PFTs) derived from the Global LAnd Surface Satellite (GLASS) products for the period 2000-2014

- Purpose and scope
  - Global monthly LAI climatology (2000-2014) derived from GLASS products, intended for use with JULES Land Surface Model and the UK Met Office Unified Model.
  - Data supports initialization, validation, and evaluation of earth system models; LAI influences energy, water, and carbon flux calculations.
  - Provides LAI per grid cell partitioned into five Plant Functional Types (PFTs) and a separate canopy height parameter; data is CF-compliant netCDF.

- Data lineage and motivation
  - Based on GLASS LAI using MODIS data (2000-2014) and AVHRR data (1981-1999) in earlier product; aims to improve seasonality and spatial consistency over previous JULES_LAI_current datasets, which showed implausible seasonal cycles in several regions.
  - GLASS LAI is preferred for its temporal and spatial consistency; this dataset uses MODIS (2000-2014) for the climatology.

- Datasets included
  - GLASS_LAI_Global_0.5deg.nc
    - Variables: Leaf Area Index (LAI) and Canopy Height (H)
    - Dimensions: month, pft (1-5 corresponding to Broad Leaf, Needle Leaf, C3 Grass, C4 Grass, Shrub), lat, lon
    - Description: 12 monthly climatological fields (2000-2014) at 0.5 degree resolution; LAI per PFT and canopy height are provided for model use.
  - Land_Cover_Frac_LC-CCI.nc
    - Variables: Canopy height (m), land_cover_class (%)
    - Dimensions: month, pseudo (1-9 representing 5 PFTs + 4 other land cover classes), lat, lon
    - Description: Fractional distribution of land cover classes per grid cell, used to partition total LAI into PFT LAIs and to define the land-cover context.

- Methodology in brief
  - Partition GLASS LAI into 5 PFTs using fractional coverage from the European Space Agency Climate Change Initiative (CCI) Land Cover product.
  - Use fixed relative weights to distribute total LAI among PFTs: Broad Leaf 5, Needle Leaf 4, C3 Grass 2, C4 Grass 4, Shrub 1 (constant across time and space in this dataset).
  - Data processing workflow:
    - GLASS LAI time series segregated into 5 PFTs with ANTS toolkit; aggregated to a 0.5° grid with Iris.
    - The resulting PFT LAIs summed to total LAI; validated against GLASS LAI (negligible loss/gain during segregation).
  - Purpose of approach: improve seasonality and overall realism of LAI within JULES, addressing earlier misrepresentations in seasonality.

- Validation and quality
  - Comparisons show strong agreement between JULES_LAI_GLASS (segregated LAI) and GLASS LAI across regions; discrepancies are within expected minor artifacts from low vegetation cover cases.
  - JULES_LAI_current (older ancillary) consistently underestimates LAI globally, underscoring improvements in the GLASS-based product.

- Format, accessibility, and structure
  - NetCDF format, CF v1.6 compliant.
  - Two files are provided together as part of the same data resource in the EIDC catalogue:
    - GLASS_LAI_Global_0.5deg.nc (LAI and canopy height)
    - Land_Cover_Frac_LC-CCI.nc (PFT/land-cover fractions)
  - Downloadable as a paired dataset to ensure consistency between LAI, canopy height, and land-cover context.

- Applications and use cases
  - Primary use: initialization, validation, and tuning of JULES and UKMO land-surface models.
  - Also suitable for other land-surface and hydrological model applications requiring globally distributed, seasonally varying LAI by PFT and associated canopy height.
  - Enables improved model representations of vegetation dynamics, energy and water balance, and carbon fluxes.

- Data governance and provenance
  - Acknowledges support from the VER A project (NERC) and the HydroJULES program.
  - Documentation links and ancillary tools (ANTS) provided for data processing lineage and reproducibility.
  - Clear provenance from GLASS MODIS/AVHRR time series to the 0.5° ancillary and final LAI product.

- Relevance to data leadership
  - Demonstrates a well-documented, open, and model-ready data asset with explicit data lineage, processing steps, and validation.
  - Addresses data-system considerations: data discoverability (paired files), metadata standards (CF-compliant NetCDF), data quality (seasonality realism, cross-product validation), and user-centric design (PFT-based LAI for model compatibility).
  - Highlights governance aspects: versioned product aligned with model configurations, clear use cases, and integration with wider data ecosystems (CCI land cover, GLASS LAI).
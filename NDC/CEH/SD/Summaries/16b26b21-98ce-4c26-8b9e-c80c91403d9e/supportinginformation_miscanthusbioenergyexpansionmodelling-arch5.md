# Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models

## Overview
- Studies yield potential and soil carbon impacts of large-scale Miscanthus bioenergy using three models: MiscanFor (Miscanthus crop growth), JULES (Dynamic Global Vegetation Model), and IMAGE (Integrated Assessment Model).
- All models run under a single climate/social scenario: SSP2-RCP2.6, with climate data downscaled/bias-corrected from HadGEM2-ES and MAGICC.
- Analyses focus on two areas and times: tropics (2040–2049) and Europe (2090–2099), to illustrate bioenergy’s role in climate mitigation (early scale-up and later bioenergy with CCS).
- Key outputs are yield and soil carbon, selected because they strongly influence life-cycle carbon balance and are common outputs across models.
- The dataset provides raw model outputs that underlie the associated publication.

## Data generation and modeling details
- Models used:
  - MiscanFor: Miscanthus crop growth model.
  - JULES: Land surface DGVM.
  - IMAGE: IAM for land-use and bioenergy dynamics.
- Climate driving data:
  - HadGEM2-ES with RCP2.6 for JULES and MiscanFor (downscaled to 0.5° and bias-corrected to WATCH climatology 1960–1999; 2006–2099).
  - IMAGE uses MAGICC-derived climate pathway, downscaled with HadGEM2-ES data from ISIMIP.
- Land-use and scenario details:
  - SSP2 land-use expansion modeled in IMAGE; rapid expansion in 2020s–2030s; maximum rate 24 Mha/yr (2035–2040); peak ~300 Mha by 2040.
- Focus areas:
  - Tropics: 25°N to 25°S for 2040–2049.
  - Europe: 15°W to 40°E and >35°N for 2090–2099.

## Data structure and formats
- Variables: bioenergy crop yield and soil carbon for each model (MiscanFor, JULES, IMAGE).
- File naming: {model}_{variable}_{period}.csv
- Formats:
  - MiscanFor: CSV
  - JULES and IMAGE: NetCDF, converted to consistent CSVs
- Grid and cells:
  - Data regridded to 0.5° resolution; 6,858 grid cells selected where any bioenergy land use occurred during the period.
  - These cells represent ~11% of global land area (Antarctica excluded); remaining 89% not modeled due to no bioenergy land use.
- Data alignment:
  - All files share identical latitude/longitude order for the 6,858 cells; not all cells have data in every file.
  - MiscanFor reports data for Europe 2090–2099 and outside Europe 2040–2049; NaN indicates missing data.

## Units and interpretation
- File columns: latitude, longitude, value (yield or soil carbon change).
- Spatial units:
  - Latitude/Longitude: degrees north/east; centers of the 0.5° grid boxes.
- Yield units:
  - Tonnes of dry matter (DM) per hectare of planted area per year.
  - MiscanFor provides yield directly; JULES/IMAGE provide biomass as tonnes C, converted to DM using 48% carbon content.
- Soil carbon change units:
  - Tonnes of soil C per hectare per year.
  - MiscanFor: per hectare of planted area; JULES/IMAGE: per hectare of entire grid box (including other land covers).

## Quality control and provenance
- Models are state-of-the-art, with rigorous testing and validation across multiple sites to ensure numerical stability and accuracy.
- Reference versions and related publications:
  - JULES: Littleton et al. 2020
  - MiscanFor: Shepherd et al. 2020
  - IMAGE: Daioglou et al. 2019; Doelman et al. 2019
  - Dataset description and related work: Littleton et al. 2022 (GCB Bioenergy)
- The dataset provides raw outputs underpinning the 2022 publication: Littleton et al., GCB Bioenergy.

## Data access, reuse, and licensing notes
- Data underpin a peer-reviewed study on Miscanthus bioenergy’s effectiveness for climate mitigation.
- JULES code is publicly available (registration required); specific version used for this dataset: r12164_biotiles_harvest.
- References provided for methodological context and model intercomparisons are included for reproducibility.

## Limitations and considerations for data stewardship
- Spatial coverage is limited to 6,858 grid cells with bioenergy land use; 89% of global land is not represented due to no bioenergy activity in the scenario.
- Data units and cross-model conversions (especially carbon content conversion) are crucial for accurate inter-model comparison.
- Missing data patterns (NaNs) reflect model domain coverage and greener field exceptions; users should account for incomplete spatial-temporal coverage in analyses.

## Practical implications for data governance
- Ensure comprehensive metadata describing grid definitions, coordinate reference system, and cell indexing to support discoverability and reuse.
- Document modeling assumptions, scenario choices (SSP2-RCP2.6), and climate driving data sources to support interpretation and governance.
- Include model provenance, versioning, and links to code/references to enable reproducibility and auditability.
- Clearly communicate scope limitations (spatial coverage and period focus) in data catalogs and data-sharing portals.
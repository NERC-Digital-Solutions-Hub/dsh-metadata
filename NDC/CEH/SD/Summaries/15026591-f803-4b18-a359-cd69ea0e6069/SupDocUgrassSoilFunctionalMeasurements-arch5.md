# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- Study of enzymatic activity in soil samples from paired intensive and extensive grassland systems across 32 sites in the UK, covering low and high pH soils.
- Samples collected in winter and spring 2015–2016; analysis conducted for a suite of extracellular hydrolytic enzyme activities using fluorescent substrates.
- Enzymes measured: Acetate Esterase, Fluorescein diacetate hydrolysis, β-glucosidase, Arylsulfatase, Phosphatase, Leucine aminopeptidase, Chitinase, and Lipase.
- All analyses performed at CEH Wallingford; data compiled and deposited as a CSV for the Environmental Information Data Centre (EIDC) as part of the NERC U-GRASS Soil Security Programme.

## Data collection and enzyme activity methods
- Sampling design: 32 UK grassland sites with land-use contrasts; soil cores (15 x 5 cm) collected along 100 m of land-use interface at 25 m intervals, 5 paired replicates per site.
- Sampling period: November 2015 to February 2016; cores stored frozen at -20°C prior to processing.
- Enzyme activity assay: conducted at CEH Wallingford using soil slurries and substrates to measure eight extracellular hydrolytic activities.
- Measurement details:
  - Substrates and enzyme pairings include acetate esterase, FDA hydrolysis, β-glucosidase, arylsulfatase, phosphatase, leucine aminopeptidase, chitinase, and lipase.
  - Reaction setup: 30 µL soil slurry + 170 µL substrate in 96-well plates; incubated 4 hours at 28°C; fluorescence measured every 30 minutes.
  - Replicates: three methodological replicates plus quenched standards; controls for fluorescence stability.
  - Output unit: nmol of product per minute per gram of dry soil.

## Data structure and contents
- File: UgrassSoilFunctionalMeasurements.csv
- Structure: 450 data rows and 12 columns.
- Columns and descriptions (selected):
  - id: unique cross-reference identifier.
  - management_intensity: qualitative descriptor of land-use management.
  - latitude: GPS coordinate (lat).
  - longitude: GPS coordinate (lon).
  - ace: nmol product min^-1 g^-1 dry soil (Acetate Esterase).
  - fda: nmol product min^-1 g^-1 dry soil (Fluorescein diacetate hydrolysis).
  - glu: nmol product min^-1 g^-1 dry soil (β-glucosidase).
  - sul: nmol product min^-1 g^-1 dry soil (Arylsulfatase).
  - pho: nmol product min^-1 g^-1 dry soil (Phosphatase).
  - leu: nmol product min^-1 g^-1 dry soil (Leucine aminopeptidase).
  - chin: nmol product min^-1 g^-1 dry soil (Chitinase).
  - lip: nmol product min^-1 g^-1 dry soil (Lipase).
- Notes: NA indicates data not recorded.
- Context: data captured from 32 grassland sites with paired management contrasts; results compiled from lab outputs and prepared for deposition at EIDC.

## Data provenance, storage, and deposition
- Lineage: soil samples collected from 32 UK grassland sites, stored at -20°C prior to processing for chemical, physical, molecular, and functional analyses; enzyme activities measured at CEH Wallingford; results compiled into an Excel file and exported as CSV for EIDC deposition.
- Purpose: support understanding of soil functional change under different management and climatic scenarios; aligns with the NERC U-GRASS programme on soil ecosystem services and resilience.
- Access and reuse: dataset prepared for deposition in the EIDC; includes explicit methodological detail to support reproducibility and secondary analyses.

## Associated files
- UgrassSoilFunctionalMeasurements.csv (data outputs for the eight measured enzyme activities across sites).

## Key data governance and stewardship considerations
- Data quality and reproducibility: detailed experimental protocol, including replication scheme, controls, and fluorescence measurement parameters; enables audit and replication of enzyme activity estimates.
- Provenance and metadata: explicit sample origin (site, management intensity, coordinates), sampling window, storage conditions, and processing steps; essential for data discovery and reuse.
- Interoperability and standards: data stored as a flat CSV with clear column descriptions; suitable for ingestion into data portals (e.g., EIDC) and integration with other soil function datasets.
- Sensitivity and limitations: temporal snapshot (single winter/spring sampling period); site-specific management contrasts; potential variability due to soil heterogeneity and BIOTA interactions; users should consider these when conducting longitudinal or comparative analyses.
- Documentation needs: ensure complete metadata (site descriptions, management intensity categories, coordinate precision, any data gaps) accompanies the CSV for discoverability and re-use.
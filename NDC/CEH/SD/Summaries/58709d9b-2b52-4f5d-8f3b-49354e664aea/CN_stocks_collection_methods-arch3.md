# Soil sampling

- Purpose: Document soil sampling, storage, analysis, and data reporting procedures for estimating soil carbon and nitrogen stocks across depth increments, to inform environmental health assessments and decision-making.

## Sampling protocol and sample handling

- Two soil samples per site collected with a 4 cm width augur, taking soil as deep as possible.
- Soil passes through a sieve with 2 mm aperture to remove stones and roots.
- Stones retained are weighed to determine the proportion of gravel and chalk flints.
- Soil cores are split into 5 cm depth increments, dried at 80 °C for 48 hours after sieving.
- Cores stored at 25 °C until processing.

## Bulk density measurement and adjustment

- Bulk density (BD) measured by weighing and calculating mass/volume.
- BD adjusted for gravel incursions using the formula:
  Adjusted BD = Unadjusted BD / 100 × (100 − % gravel)

## Carbon and nitrogen analysis

- Each depth fraction ground in a ball mill (25 s−1 for 2 minutes).
- Carbonates removed by treating with 10% HCl (dropwise until effervescence ceases).
- Samples redried; ~10 mg used for combustion analysis.
- Analysis performed with an Elementar Vario EL combustion analyser, calibrated with acetanilide standard (10.45% N, 71.4% C).
- QC: Standards and blanks run every 20 samples; 5% analytical replicates included.

## Stock calculation (per depth)

- Carbon and nitrogen stocks calculated for each soil depth using measured C and N percentages, corrected bulk density, and core depth to yield stocks in tonnes per hectare (C t ha and N t ha).
- The calculation uses core depth, corrected bulk density, and the raw C and N percentages (post-acid treatment where applicable).

## Quality control and data management

- Quality control data: Standards and blanks every 20 analyses; 5% replicates.
- Data file: Soil_C_budgets_to_depth.csv, with metadata definitions for fields:
  - Land Use (land use type)
  - Site (site identifier)
  - Replicate (1 or 2)
  - Soil level (top, middle, bottom)
  - Soil Depth from surface (5 cm increments)
  - Core depth (length of core)
  - Core diameter (diameter of augur)
  - Core volume (πr^2h)
  - Dry wt (soil weight per increment)
  - Gravel wt (weight of stones >2 cm)
  - % gravel (fraction of core occupied by gravel)
  - Bulk density with gravel
  - BD corrected for gravel
  - N post acid (total nitrogen after carbonate removal)
  - C post acid (total carbon after carbonate removal)
  - C t ha (carbon in tonnes per hectare)
  - N t ha (nitrogen in tonnes per hectare)
  - CN post acid (carbon to nitrogen ratio after carbonate removal)

## Relevance to monitoring and governance

- Provides a structured, auditable protocol for deriving soil C and N stocks across depths, enabling monitoring of environmental health indicators.
- Includes explicit metadata for each data field to facilitate data sharing, interpretation, and reuse.
- Emphasizes quality control practices and transparent data processing steps, supporting data governance and standards compliance.
- Recognizes data-related barriers relevant to monitoring frameworks, such as data availability, metadata adequacy, and the burden of data transformation and sharing.
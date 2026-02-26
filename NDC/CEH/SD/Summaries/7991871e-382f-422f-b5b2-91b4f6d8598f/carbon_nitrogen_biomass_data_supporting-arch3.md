# Carbon_Nitrogen_Biomass_data_Supporting.docx

## Overview
- Dataset from an ex situ experiment testing growth (mass) and carbon and nitrogen concentrations in birch (Betula pendula) and Scots pine (Pinus sylvestris) seedlings.
- Soils sourced from forest stands that are monocultures of pine, monocultures of birch, or a 1:1 mixture.
- Aims aligned with environmental monitoring: track how stand type and soil context influence seedling biomass and foliar C:N metrics.

## Study site and experimental design
- Location: Hambleton Forest, Forestry Commission managed site in Yorkshire, UK (54°13' N, 001°07' W).
- Stand structure: three replicates each of silver birch-only, Scots pine-only, and mixed (1:1) stands; each stand ~0.2 ha with 900 trees per stand; mixed stand planted in a checkerboard pattern.
- Ex situ setup: on 19 September 2019, ten replicate soil samples (5 cm x 5 cm, 20 cm deep) from each stand type were collected.
- Seedling establishment: soil samples used to prepare seedling tubes containing two pine seeds, 4–10 birch seeds, or a mixture (2 pine + 2–6 birch seeds) per tube; seeds stratified and surface-sterilized prior to use.
- Growth conditions: growth chamber at 18°C with 16 hours light/8 hours dark; watered as needed.
- Harvest: 19–22 weeks after seed addition; seedlings assessed for potential mycorrhizal status (mycorrhizal vs non-mycorrhizal).
- Post-harvest processing: shoots dried at 60°C; roots stored for future analyses; foliar C:N ratio measured using a Vario EL Cube.

## Data organization and variables
- Data structure: organized in columns with five key headers:
  - Plot_replicate
  - Stand (Pine, birch, or mixed)
  - Tube_content (Pine only, birch only, or mixture)
  - Seedling (pine or birch)
  - Replicate (individual ex situ system derived from each plot)
- Measured/recorded variables:
  - foliar_CN_ratio: foliary carbon to nitrogen ratio
  - mass_g: dry mass of individual seedlings (roots and shoots)
  - myc_status: whether ectomycorrhizal associations were observed on roots (Myc) or not (NM)
  - %N: nitrogen concentration in foliage
  - %C: carbon concentration in foliage
- Notes on data specifics:
  - When a tube contained the same species, data reflect the average of seedlings harvested from that tube.
  - Seedling counts/tube contents varied to ensure adequate root coverage within tubes.

## Measurements and processing
- Primary measurements:
  - Foliar carbon and nitrogen concentrations (%C, %N)
  - Foliar C:N ratio
  - Dry shoot/root mass (mass_g)
  - Mycorrhizal association status (myc_status)
- Sample handling:
  - Seedlings harvested from tubes 19–22 weeks after seed addition
  - Shoots dried for mass measurements; roots stored for future analyses
- Analytical instrument: Vario EL Cube used for foliar C and N analyses

## Dataset reference
- Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine (Pinus sylvestris L.) and silver birch (Betula pendula Roth.) in northern Britain. Annals of Silviculture Research 40:11-18

## Relevance for monitoring frameworks
- Provides a structured example of linking stand-type context (pine, birch, mixed) to seedling performance and leaf chemistry under controlled conditions.
- Demonstrates explicit data organization for monitoring datasets: standardized headers, clearly defined categorical and numerical variables, and explicit treatment/sowing conditions.
- Highlights the integration of biotic status (mycorrhizal association) with growth and chemical metrics, useful for evaluating ecosystem health indicators and forest management decisions.

## Data quality, governance, and sharing considerations
- Metadata and data organization are clearly described, aiding traceability and reproducibility.
- Data are stored with explicit treatment definitions and replication structure, supporting transparency in data sharing.
- Potential governance considerations for monitoring datasets include maintaining up-to-date metadata, ensuring data sharing aligns with openness standards, and preserving linkages between stands, tube contents, and replication.
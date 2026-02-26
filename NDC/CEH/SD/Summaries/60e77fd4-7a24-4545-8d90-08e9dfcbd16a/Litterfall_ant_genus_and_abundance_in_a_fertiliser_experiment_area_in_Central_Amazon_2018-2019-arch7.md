# Litterfall ants data spreadsheet for the AFEX experiment in KM41, BDFFP

## Overview
- Dataset resulting from the Amazon Fertilization Experiment (AFEX) within the KM41 reserve of the Biological Dynamics of Forest Fragments Project (BDFFP).
- Focuses on ant community data collected inside 50x50 m fertilized plots, across multiple treatments and blocks, with annual sampling in two years (2018 and 2019).

## Spatial context and study design
- Location: KM41 reserve, ~100 km from Manaus, Brazil; coordinates around 02 24'S, 59 52'W.
- Environment: humid/wet tropical forest (dense Terra Firme); soils are red-yellow podzols and ferrasols.
- AFEX experimental layout:
  - Treatments: 7 fertilization treatments plus a control (total of 8 treatment categories: Control, N, P, CAT, N+P, CAT+N, CAT+P, CAT+N+P).
  - Replication: 4 replicates per treatment, totaling 32 plots.
  - Spatial arrangement: 4 blocks with plots at least 250 meters apart.
  - Plot size: 50 x 50 meters; sub-plots within plots are 1 x 1 meter (five sub-plots per plot, arranged within each plot).

## Data collection and ant sampling
- Ant sampling within each plot:
  - Five 1x1 m sub-plots per 50x50 m plot (total of 20 sub-plots per treatment, 160 sub-plots overall).
  - Method: Winkler extractor; 48-hour extraction from litter samples.
  - Preservation: ants fixed in 90% alcohol.
  - Identification: by subfamilies and genera using standard taxonomic keys; species-level identifications cross-checked with AntCat and INPA collections.
  - Sampling years: 2018 (October) and 2019 (September) — two annual samplings during the dry season.

## Data product: Litterfall ants spreadsheet
- Primary dataset: litterfall_ants.csv.
- Core schema (example columns):
  - YEAR: Year of sampling (e.g., 2018, 2019).
  - BLOCK: Block identifier (1–4).
  - PLOT: Plot identifier within a block (1–5).
  - TRT: Treatment or combination applied to the plot (as defined in AFEX section).
  - SUBFAMILIES: Ant subfamily data.
  - GENERA: Ant genera observed.
  - INDIVIDUAL: Count of individuals.
- Data content structure:
  - Records are organized to capture per-plot, per-subplot, per-year counts across subfamilies and genera.
  - Example entries include taxa such as Ponerinae, Myrmicinae (e.g., Crematogaster), Nylanderia, Hypoponera, Gnamptogenys, etc.
- Temporal coverage: two sampling events (2018 October; 2019 September).

## GIS-related insights and potential analyses
- Spatial features to map and analyze:
  - Plot boundaries and layouts (50x50 m plots; 4 blocks; inter-plot spacing).
  - Treatment assignments by plot (to examine spatial patterns of fertilization).
  - Sub-plot locations within each plot (1x1 m points for sampling data).
- Possible GIS workflows:
  - Create a geodatabase with polygon features for plots and points for sub-plots; join ant counts to the corresponding plot by YEAR, BLOCK, PLOT, and TRT.
  - Generate per-plot metrics (richness, abundance, evenness) by year and treatment; map spatial distribution of ant diversity across AFEX plots.
  - Integrate environmental context (soil type, climate zone, vegetation type) to analyze correlations between ant communities and habitat variables.
  - Compare spatial patterns of ant assemblages across treatments and blocks to assess treatment effects on biodiversity.
- Data harmonization considerations:
  - Align multiple data sources (plot design, fertilization regime, taxonomic identifications) with consistent identifiers (YEAR, BLOCK, PLOT, TRT).
  - Handle potential resolution differences between plot-level treatments and sub-plot-level sampling records.

## Data quality, standards, and references
- Taxonomic references and keys used for ant identification (e.g., Baccaro et al. 2015; Bolton AntCat).
- Sampling methodology standardized (Winkler extractor, 48-hour processing, fixation in alcohol).
- Data provenance includes explicit documentation of plot-level treatments, block arrangement, sampling years, and sub-plot layout.
- Related environmental context and soils/climate information drawn from published literature on the BDFFP KM41 area and Amazon soils.

## Additional notes
- The dataset is embedded within a broader field study of fertilization effects on forest dynamics and invertebrate communities, offering rich spatial and temporal dimensions for GIS-enabled analysis and visualization.
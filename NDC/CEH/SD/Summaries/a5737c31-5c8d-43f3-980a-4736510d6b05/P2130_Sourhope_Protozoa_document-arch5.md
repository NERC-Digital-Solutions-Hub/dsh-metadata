# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

## Purpose and scope
- Describes soil protozoan abundance and diversity data collected during the NERC Soil Biodiversity Thematic Programme at Sourhope, Scotland (1999-2000).
- Aims to understand soil protozoan diversity and their functional roles in carbon and nitrogen turnover.
- Data originate from a single intensive field site with a structured experimental design, intended to enable discovery and reuse of protozoan community data.

## Study context and site description
- Location: Sourhope Research Station, Macaulay Land Use Research Institute (now James Hutton Institute), Scottish Borders.
- Site characteristics: mid-altitude temperate upland grassland on base-poor, damp mineral soils; grid reference NT8545019630.
- Experimental design: five blocks; each block contains six main plots (total of 30 plots).
- Sampling framework: soil sampling occurred on multiple dates (including March 1999, May 1999, July 1999, September 1999, and July 2000; six occasions for some datasets).
- Soil and vegetation context recorded to link protozoan data to soil properties and vegetation classification.

## Data collection methods and protocols
- Focus: protozoan groups including naked amoebae, testate amoebae, ciliates, and flagellates.
- Sample processing: soil collected from 2 x 2 m sub-plots; multiple sub-samples composited; air-dried and incubated to extract protozoa.
- Extraction and enumeration: different protocols for live and dead tests, amoebae, ciliates, and flagellates; incubations conducted in controlled conditions (temperature around 15 °C; dark).
- Output metrics: counts per gram dry weight of soil (or per gram of oven-dried soil) for each protozoan group; both direct and indirect enumeration methods reported where applicable.
- Laboratory analysis: conducted at the Centre for Ecology & Hydrology, Ferry House, Windermere, Cumbria; procedures include staining, settling/counting chambers, and enrichment/culture steps for certain groups.
- Data quality checks: numeric range checks, formatting checks, and logical integrity verifications applied to datasets.

## Datasets included and key contents
- Dataset 1050: All Protozoa Abundance July 2000 (P2130_PROTOZOA_ABUND_JULY2000.csv)
  - Single-occasion enumeration from 25 re-wetted soil samples across sub-plot S of plot 4D (Sourhope) on 17 July 2000.
  - Key fields: SUID, BLOCK, MAIN_PLOT, TREATMENT, SAMPLE_NUMBER; abundances for naked amoebae, direct/indirect/average flagellates, live/dead testate amoebae, ciliates; unit: thousands per gram dry weight (or as specified); soil status: Air Dried.
- Dataset 1051: All Protozoa Abundance (P2130_PROTOZOA_ABUNDANCE.csv)
  - Enumeration across six occasions from 25 plots at Sourhope (1999-2000).
  - Key fields: SUID1/SUID2, SAMPLING_DATE, BLOCK, MAIN_PLOT, TREATMENT; abundances for naked amoebae, direct/indirect flagellates, flagellates average, live/dead testate amoebae, ciliates; units as in 1050.
- Dataset 1052: Protozoa Species Size Distribution (P2130_PROTOZOA_SPECIES_SIZE.csv)
  - Average numbers of protozoa and average numbers of different protozoan species by cell length size classes, across six sampling occasions.
  - Key fields: SIZE_RANGE (12 size classes), NAKED_AMOBA_ABUNDANCE, NAKED_AMOBA_SPECIES, FLAGELLATES_ABUNDANCE, FLAGELLATES_SPECIES, TESTATE_AMOEBA_ABUNDANCE, TESTATE_AMOEBA_SPECIES, CILIATES_ABUNDANCE, CILIATES_SPECIES; soil status and data type noted.
- Dataset 1053: Protozoa Size Distribution (P2130_PROTOZOA_SIZE_DIST.csv)
  - Enumeration by cell length for six occasions across 25 plots.
  - Key fields: SAMPLING_DATE, SIZE_RANGE (cell-length classes), NAKED_AMOBA, FLAGELLATES, TESTATE_AMOBA, CILIATES; each with abundance and species-related metrics.
- Dataset 1054: Protozoan species diversity by plot (130_PROTOZOAN_SPEC_DIVERSITY.csv)
  - Protozoan group (e.g., ciliates, testate amoebae) detected per plot over six sampling occasions.
  - Key fields: BLOCK, MAIN_PLOT, PROTOZOAN_GROUP, GENUS, SPECIES, SPECIES_OCCURRENCE, NUMBER_OF_PLOTS.

## Data structure and metadata
- File format: Comma-separated values (CSV).
- Core identifiers: Sampling Unit IDs (SUID/SUID1/SUID2), BLOCK, MAIN_PLOT, TREATMENT, SAMPLING_DATE.
- Variables cover abundance counts, presence/absence, species counts, and size-class distributions.
- Units: per gram dry weight of soil (or as specified per dataset); soil status indicates air-dried status for many measures.
- Provenance: Laboratory work performed at EH, Windermere; data archiving and project references linked to Scott et al. 2003 and related literature.

## Quality control and limitations
- Quality assurance steps include numeric range checks, formatting checks, and logical integrity checks.
- NERC provides the data with standard QA but does not warrant accuracy or fitness for a particular use.
- Users should interpret results with caution regarding data accuracy and potential limitations of the underlying measurements and soil sampling context.

## Governance, sharing, and caveats for data stewards
- Metadata is detailed (site, plot design, sampling dates, treatments), aiding dataset discoverability and reuse.
- Clear documentation of measurement methods, units, and data fields supports interoperability and re-use in meta-analyses or integrated soil biodiversity studies.
- Caveat: data come with liability limitations from NERC; users should validate suitability for intended applications and acknowledge provenance.

## Related references and resources
- Primary publications and handbooks for Sourhope field data and soil biodiversity context (e.g., Scott et al., 2003; Finlay et al., 2000; Usher et al., 2006).
- Laboratory protocol references and site descriptions provide deeper provenance for data interpretation and replication.
- Data availability is anchored to the Sourhope field experiment dataset suite and associated project outputs.
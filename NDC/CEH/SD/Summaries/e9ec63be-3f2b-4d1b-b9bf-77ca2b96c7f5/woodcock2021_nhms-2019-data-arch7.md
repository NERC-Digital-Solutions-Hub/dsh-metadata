# Data describing pollen identified from honey samples originating from the UK CEH National Honey Monitoring Scheme for 2019

## Overview
- Describes regional and temporal occurrence of plants foraged upon by managed honey bees (Apis mellifera) in 2019.
- Derived from DNA metabarcoding of pollen extracted from honey samples collected under the UK National Honey Monitoring Scheme (NHMS).
- First full year of NHMS data; future years will be released as processing completes.
- Funded by NERC and BBSRC under the ASSIST program.

## Data content and structure
- Taxonomy.csv: Taxonomic affiliations of plant species identified via DNA metabarcoding; includes full binomial names, lowest taxonomic level reached (species/genus/family), and taxonomic identifiers (BRCcode, NBN_ID).
- NHMS_2019_Regional_data.csv: Regional data by country/region (NUTS1 level) with average DNA reads per species, plus additional regional metadata:
  - Country, Region, Yield (hive yield in kg), Percentage sugar, Percentage water
  - Disease probabilities: VROA_Had_It (Varroa mite) and DFWV_Had_It (Deformed Wing Virus)
  - Species names (see taxonomy.csv) with DNA read counts
- NHMS_2019_Seasonal_data.csv: Seasonal data by country and month (e.g., M04–M11) with similar fields to regional data:
  - Country, Month, Yield, Percentage sugar, Percentage water
  - Disease probabilities (VROA_Had_It, DFWV_Had_It)
  - Species names (see taxonomy.csv) with DNA read counts
- Data are presented as DNA read counts per plant species, with Brassica reads tracked as a covariate for downstream analyses.
- NA indicates missing data in applicable fields.

## Methods and QA
- NHMS: 535 honey samples from England, Wales, Scotland, and Isle of Man in 2019; samples collected from both hobbyist and professional beekeepers.
- Sampling: honey scraped from recently filled comb cells; metadata on location and time collected via an online portal; sample submission followed by QA procedures.
- Archiving: all samples stored long-term in the NHMS archive at CEH Wallingford.
- Metabarcoding workflow (HONEYPI): DNA extraction, amplification, Illumina MiSeq sequencing; ASV-based processing with DADA2; removal of conserved ITS2 flanking regions; taxonomic classification against an in-house ITS2 database.
- Data integration: ASV tables can be merged across sequencing runs without re-clustering, enabling regional/seasonal data aggregation.
- Data provenance and references provided for methodological details (Oliver et al. 2021; Kozich et al. 2013; McMurdie & Holmes 2013; Sickel et al. 2015).

## Geographic and temporal coverage
- Spatial: UK regions including England (multiple regions), Scotland, Wales, and Isle of Man (data organized at Country and NUTS1 regional level).
- Temporal: Data framed around monthly sampling periods (Seasonal data) and regionally aggregated data; first full year is 2019 with months indicated (e.g., M04–M11 for April–November in various regions).

## Data quality, limitations, and considerations for GIS use
- Taxonomic resolution varies (species, genus, or family level) per sample.
- Some metadata (yield, disease data) may be incomplete for certain samples or regions/months.
- Regional/monthly data reflect beekeeper-reported yields and integrated disease probabilities, which may introduce reporting biases alongside molecular pollen identifications.
- The dataset is limited to 2019, with future years to be added as processing completes.
- Data are suitable for map-based visualization of forage plant diversity and bee foraging patterns when joined with regional boundaries and seasonal layers.

## GIS relevance and how to use
- Enables mapping of plant foraging by honey bees across UK regions and over time using DNA-read counts as a proxy for plant occurrence.
- Can be linked to other GIS layers (habitat, land use, phenology, climate) to analyze foraging patterns, plant diversity in bee diets, and potential ecological drivers.
- Regional and seasonal data support thematic maps of:
  - Plant taxa richness and composition by region and month
  - Forage contribution of Brassica crops (covariate)
  - Bee colony health indicators (Varroa and Deformed Wing Virus probabilities) by region and time
  - Honey yield and honey characteristics (sugar, water content) in relation to foraged flora

## Access, provenance and references
- Data archived and described as part of the UK National Honey Monitoring Scheme (NHMS) with supporting QA and processing pipelines (HONEYPI).
- Core methodological references:
  - Kozich et al. (2013)
  - McMurdie & Holmes (2013)
  - Oliver et al. (2021)
  - Sickel et al. (2015)
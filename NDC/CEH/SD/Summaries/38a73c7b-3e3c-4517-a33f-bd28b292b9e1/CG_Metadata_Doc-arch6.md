# Survey of British calcareous grasslands, 1990 and 2007

- A national survey of calcareous grasslands in Great Britain conducted in two periods: 1990–1993 and 2006–2009, designed to be repeatable with minimal observer bias and to cover a wide climatic and deposition gradient.
- Purpose: collect standardized vegetation and soil data to understand how climate, air pollution, and nitrogen deposition affect calcicolous ecosystems; data suitable for analysis, comparison with British Vegetation Classification (NVC), and broader ecological research.

## Dataset overview

- Data components:
  - CG_SITES.csv: Site-level information for each plot, including plot ID, site name, status, year, grid references, NVC type, soil pH, altitude, aspect, slope, coastal indicator, soil chemistry (organic content, ammonium, nitrate), average soil depth, soil type, and notes.
  - CG_VEG.csv: Vegetation species data per plot per year, including plot ID, year, species recorded, taxonomic references, count (frequency of occurrence across 36 quadrats per plot), and growth form classification.
- Scope:
  - Geographic coverage: Britain (Great Britain).
  - Plots: 128 plots surveyed in 1990; 48 plots resurveyed in 2007; 121 plots data available for 1990 due to loss of data from seven plots (four sites).
  - Species data: 1990 dataset includes bryophytes and lichens; 2007 dataset excludes bryophytes (and lichens not noted).
- Data origin and references:
  - 1990 survey originated from DoE contract; 2007 survey funded by NERC.
  - Key publications and data centre references provided; dataset archived in the NERC Environmental Information Data Centre (EIDC) with DOI: 10.5285/38a73c7b-3e3c-4517-a33f-bd28b292b9e1.
- Data access:
  - Datasets are available as CG_SITES.csv and CG_VEG.csv through the NERC EIDC resource accompanying the Survey of British calcareous grasslands, 1990 and 2007.

## Sampling design and methods

- Plot design:
  - Standard 12 x 12 m grids (rarely 6 x 24 m); each plot subdivided into four 6 x 6 m blocks, then into nine 2 x 2 m units.
  - Within each 2 x 2 m unit, a 0.5 x 0.5 m quadrat is used; total of 36 quadrats per plot.
  - Permanent plot relocation markers: seven loops of insulated copper wire buried 5–15 cm deep to enable relocation; markers designed for durability and relocation accuracy (~5 cm relocation precision).
- Vegetation recording:
  - Presence/absence (count/frequency) data collected for vascular plants, bryophytes, and macro-lichens (as applicable per year).
  - For each quadrat, height and percent cover of vegetation estimated; dominant species noted with cover emphasis; growth form categorized (e.g., grasses, forbs, bryophytes, lichens).
  - Species grouped into grasses, other herbs, and lower plants; vouchers taken for difficult taxa; inflorescences recorded but not in all cases.
  - Recording time per plot ranges from 3 to 12 hours; grid setup typically 45 minutes; data management via VESPAN II.
- Soil sampling and analyses:
  - Top 10 cm soil sampled at plot locations corresponding to copper marker loops.
  - 1990: field pH measured in situ; 2007: soil samples collected (composite of five subsamples), stored at 4°C, processed in the lab.
  - Analyses included soil pH (water and extract), plant-available phosphorus (Olsen-P), nitrate and ammonium, base cations (Ca, Na, Mg, K), aluminum, organic matter (loss on ignition), and moisture-adjusted corrections.
  - Extracts used for chemical analyses; data emphasize plant-available fractions (NaCl extracts and Olsen-P data discussed in publications).
- Data handling and quality:
  - Data handled with software tools (VESPAN II) to ensure repeatability and comparability.
  - The methodology aims for detector-like repeatability with low observer bias; results align with NVC constancy classes, though certain taxa constancies may be underrepresented for less frequent species.

## Data structure and content details

- CG_SITES.csv:
  - PLOT_ID, PLOT, SITE, STATUS, YEAR, OSGR, EASTING, NORTHING, NVC, PH, ALT, ASPECT, SLOPE, SCREE, PH_LE_6, COASTAL, NOTES, ORG, AMMONIUM, NITRATE, AVE_SOIL_DEPTH, SOIL_TYPE
  - Data types include text and numeric; 999 denotes missing data.
  - Provides site-level environmental context and soil chemistry metrics.
- CG_VEG.csv:
  - PLOT_ID, PLOT, YEAR, SPECIES_REC, BRC_NUM, BRC_NAME, COUNT, GROWTH
  - Records cumulative presence/absence counts per species across 36 quadrats per plot/year; up to 36 occurrences per plot.
  - Growth form categorization facilitates higher-level ecological analysis.
- Plants and taxa context:
  - 1990 data include bryophytes and lichens; 2007 data exclude bryophytes, affecting cross-year comparability for those groups.
- Metadata and taxonomic references:
  - BRC_NUM and BRC_NAME linked to PlantAtt and BryoAtt references for taxon attributes where available.

## Data quality, caveats, and limitations

- Data completeness:
  - Original data recovered for 121 plots in 1990; seven plots’ data were lost, reducing 1990 data completeness.
- Taxonomic coverage:
  - Bryophytes included in 1990 but absent in 2007; macro-lichen data included where possible; potential inconsistencies across years for certain taxa.
- Methodological considerations:
  - The 36-quadrat frequency approach emphasizes presence/absence rather than explicit percentage cover, with constancy classifications aligned to British Plant Communities (NVC).
  - The method is unique and not directly comparable to all other vegetation datasets.
  - Potential issues with marker loss due to treasure-hunting or ground disturbance; lack of comprehensive canopy cover estimates.
- Relocation and field conditions:
  - Relocation accuracy ~5 cm, with some variability due to uneven terrain.
  - Plot placement aimed at representativeness and ease of relocation while capturing a range of conditions (aspect, altitude, slope).

## Potential uses, data products, and reuse considerations

- Suitable analyses:
  - Longitudinal comparisons of vegetation and soil parameters across 1990 and 2007 at plot and site scales.
  - Examination of climate change and air pollution effects on calcicolous grasslands using species frequencies and soil chemistry data.
  - Evaluation of relationships between soil chemistry (pH, nutrients) and vegetation composition, including NVC alignment.
- Data products that Data Support professionals could create:
  - Cleaned, merged datasets combining CG_SITES and CG_VEG with consistent year alignment and taxonomic harmonization.
  - Interactive dashboards or pivot-table-ready outputs enabling end users to explore plot-level vegetation and soil data by year, site, or habitat type.
  - Documentation and data dictionaries detailing variable definitions, units, and methodological notes to facilitate reuse by non-specialists.
- Integration opportunities:
  - Link with other national vegetation surveys and environmental data (e.g., atmospheric deposition, climate variables) for broader ecological analyses.
  - Cross-walk with NVC profiles to assess community changes over time.
- Provenance and citation:
  - Dataset curated and published in NERC EIDC (2015); primary publications cited for methodological validation and context.
  - Appropriate acknowledgment to Rich et al. and Malloch et al. in any derivative analyses or products.
# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Purpose, design and scope
- Provides data on caterpillar masses from two feeding guilds (hedgerow and grass-margin feeders) under streetlight treatments to assess effects of artificial light at night (ALAN).
- Matched-pairs design across lit and unlit habitats in hedgerows and grass margins; 26 site pairs and one triplet where lit and unlit sections were otherwise identical.
- Lighting treatments reflect regional practice: predominantly LED and high-pressure sodium (HPS), with two low-pressure sodium (LPS) sites; lit transects illuminated for at least five years prior to sampling.
- Sampling conducted across two seasons/times to capture phenology: spring beating for woody-vegetation feeders; winter sweep netting for grass-margin feeders.
- Night-time sampling between 21:00 and 06:30, on cloudily conditions or new moon, with additional lux measurements to quantify light environment.

## Site selection, lighting, and environmental controls
- Site matching via GIS overlays of street lighting and satellite imagery to identify linear habitat sections with lit vs unlit comparators; final matching produced 26 lit/unlit pairs and one triplet.
- Pairs located within 60–527 m of each other (median ~118 m) to ensure similar microclimates; transects placed along straight roads with minimal angular difference.
- Attempts to control confounds: comparable hedgerow age structure, vegetation height in grass margins, adjacent habitat quality, and local agricultural management within each pair.
- Hedgerow and grass-margin transects sampled with careful consideration of habitat structure (dominant plant species and hedgerow features for hedgerows; vegetation height for grass margins).

## Lighting measurements and spectral data
- Light intensity measured with lux meters at five points along each transect, at heights relevant to caterpillar exposure (1.25 m for hedgerows; 0.25 m for grass margins).
- Reported lux ranges: hedgerows 1.42–15.84 lux (mean 5.7 lux); grass margins 0.18–7.14 lux (mean 2.2 lux); unlit transects <0.01 lux.
- Spectral analyses conducted only for grass margins using a spectrometer; reported Correlated Colour Temperature (CCT) estimates: LED 2700–4000 K (warmer to neutral white); HPS ~2200 K; LPS ~1800 K. Authors note lux does not capture full spectral ecology for insects.

## Sampling methods and timing
- Hedgerow beet/beating: spring sampling to target spring-feeding caterpillars; multiple points along transects with either drainpipes or beating trays; sampling adjusted to maintain consistent fertility of the guilds.
- Grass margins: winter sampling with sweep nets to capture overwintering noctuids on grasses; transects walk at a steady pace with a continuous figure-of-eight sweep pattern.
- Sampling windows chosen to minimize phenological artifacts: late spring for hedgerows; winter for grass margins; several visits per site to build sufficient counts.
- Sampling effort: lit and unlit transects sampled an approximately equal number of times; some sites had schedule changes (e.g., one site received new lighting during the study).

## Specimens, measurements, and data structure
- Specimens: all caterpillars weighed (milligrams) after collection; grass margins mean mass ~98 mg; hedgerow mean mass ~43 mg.
- Taxonomic resolution: caterpillars assigned provisional identifications and grouped into 20 hedgerow units and 16 grass-margin units, including some day-flying species with nocturnal larval stages.
- In total: 826 caterpillars from grass margins and 1021 from hedgerows retained for weighing; most early spring samples could not be retained due to Covid-19 restrictions.
- Data files:
  - Boyes_et_al_2021_hedgerows_mass.csv (hedgerow caterpillar counts/masses)
  - Boyes_et_al_2021_grass_mass.csv (grass margin caterpillar counts/masses)
  - Boyes_et_al_2021_field_sites_data.csv (site-level metadata)
- Key fields (examples):
  - Visit_ID, Site_ID, Treatment, Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince (grass margins)
  - Old_Site_ID, SiteID_Fig, Sampling_meth, Site_Name, Light_Type, Lit_transect_centroid/E/N/lat/long, Unlit_transect_Centroid/E/N/lat/long
  - Hedgerow-specific: hedgerow illumination, distance between lit/unlit transects, urban area metrics at 100/250/500 m radii, etc.
- Data organization supports linkage between site-level metadata and caterpillar-level observations, with precise geographic coordinates and light treatments for each transect.

## Data quality assurance and processing
- Standardized field protocols and same-night sampling to reduce temperature effects.
- Data entry conducted in Excel with dropdowns and rules to minimize entry errors; entries double-checked and outliers screened.
- Specimens identified by the lead author using existing resources; samples retained at -20°C (except some 2020 samples missed due to Covid-19).
- Clear documentation and a data dictionary accompanying the CSV files to facilitate reuse and interpretation.

## Data governance, licensing, and provenance
- Data linked to the 2021 publication: Boyes et al. and related methodological references on ecological light pollution.
- Licensing: reproduced content from the linked study under CC BY-NC; data themselves are described for reuse with appropriate attribution (non-commercial use).
- Provenance: comprehensive metadata capture (sampling methods, sites, light types, GPS-like coordinates, lux readings, and taxonomic groupings) to support replication and re-use.
- Accessibility: data provided as CSV files with a detailed data dictionary and field-site data to enable dataset discovery and integration with other data holdings.

## Considerations for data stewardship and reuse
- Lux as a surrogate for ecologically relevant illumination has limitations; spectral data are partially available and grass-margin data include spectral measurements only for that habitat.
- Taxonomic resolution is provisional and grouped into functional units; users should consider potential uncertainties in identifications.
- Data are suitable for meta-analyses on ALAN effects across habitats, while capitalizing on the explicit matched-pairs design and long-term lighting consistency.

## References
- Boyes, D.H., Evans, D.M., Fox, R., Parsons, M.S., & Pocock, M.J.O. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle. Insect Conservation and Diversity, 167-187.
- Longcore, T. & Rich, C. (2004) Ecological light pollution. Frontiers in Ecology and the Environment, 2, 191-198.
- Maudsley, M., Seeley, B., & Lewis, O. (2002) Spatial distribution patterns of predatory arthropods within an English hedgerow...
- Merckx, T. & Van Dyck, H. (2019) Urbanization-driven homogenization...
- Porter, J. (2010) Colour Identification Guide to Caterpillars of the British Isles...
- Staley, J.T., et al. (2016) Little and late: How reduced hedgerow cutting can benefit Lepidoptera.
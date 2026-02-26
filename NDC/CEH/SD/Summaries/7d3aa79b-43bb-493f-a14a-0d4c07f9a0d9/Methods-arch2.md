# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Field study comparing moth caterpillar communities in lit vs unlit habitat sections (matched-pairs design) across two habitat types: hedgerows and grass margins.
- 26 lit/unlit site pairs plus one triplet; lit sections illuminated by LED, high-pressure sodium (HPS), and two low-pressure sodium (LPS) sites; all lighting treatments in place for at least five years.
- Sites chosen to minimize urbanization confounds; lit/unlit transects separated by ≥60 m (median 118 m).
- Sampling occurred across two seasons and periods to capture different caterpillar life stages; field nights confirmed no part-night lighting.

## Lighting, spectra, and measurements
- Light intensity measured with lux at five points along each transect, at heights relevant to caterpillars: 1.25 m (hedgerows) and 0.25 m (grass margins).
- Reported mean lux: hedgerow lit transects 1.42–15.84 lux (mean 5.7 lux); grass margin lit transects 0.18–7.14 lux (mean 2.2 lux). Unlit transects <0.01 lux.
- Spectral data collected for grass margins using a spectrometer; estimated Correlated Colour Temperature (CCT): HPS ~2200 K, LPS ~1800 K, LED ~2700–4000 K.
- Acknowledges lux limitations as a human-vision metric that may not capture ecologically relevant spectra for insects.

## Site matching and habitat controls
- Pairs matched for habitat type, distance, and microhabitat features; hedgerow trees presence, vegetation height, and adjacent high-quality habitat were controlled or exclusions applied to ensure comparability.
- For hedgerows: recorded dominant woody plant species, hedge height/width; for grass margins: vegetation height measured to ensure similar management between lit/unlit transects.

## Caterpillar sampling methods
- Hedgerows: spring beating (three 14 m points per transect) to sample deciduous-wood feeders; two beating methods used (drainpipes or beating tray).
- Grass margins: winter sweep-net sampling of noctuid caterpillars on grasses and low vegetation; transects ~14 m, sometimes longer to match habitat; sampling conducted mainly 21:00–06:30 on mild nights (min temp ≥ 6°C).
- Sampling schedule: hedgerow sampling in spring (May 2019, April 2020) and grass-margin sampling in winter 2018–2019; most sites sampled multiple times (mean visits per site variable, designed for balanced lit/unlit comparisons).
- Specimens: all caterpillars weighed (grams to 0.0001 g) and provisionally identified; grass-margin samples included day-flying taxa with nocturnal larval stages.

## Taxonomic resolution and masses
- Hedgerow caterpillars: predominantly winter-flying geometrids and some micromoths; grouped into 20 taxonomic units.
- Grass margin caterpillars: predominantly overwintering noctuids; grouped into 16 taxonomic units.
- Day-flying Lepidoptera (34 units) included due to nocturnal larval stages potentially affected by ALAN.
- Mean masses: grass-margin caterpillars 98 mg (range 0.07–2,240 mg); hedgerow caterpillars 43 mg (range 0.2–866 mg).

## Data collection, quality control, and structure
- Data collection forms standardized; field data transcribed to Excel with dropdowns and validation; data entry completed within 24 hours of field visits.
- Data quality: records double-checked for entry errors and outliers; samples stored at -20°C (COVID constraints affected retention for 2020 spring samples).
- Main data files:
  - Boyes_et_al_2021_hedgerows_mass.csv (hedgerow caterpillar counts)
  - Boyes_et_al_2021_grass_mass.csv (grass margin caterpillar counts)
- Field data and metadata files:
  - Boyes_et_al_2021_field_sites_data.csv (site-level metadata, light type, transect coordinates, illumination measurements, urban metrics within 100/250/500 m radii, transect distances)
- Key fields include: Visit_ID, Site_ID, Treatment (unlit/LED/HPS/LPS), Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince; site fields cover light type, transect centroids, hedgerow/grass metrics, urban-area classifications, and radii-based urban proportions.
- Data structure notes:
  - Spectral data limited to grass margins (grass margin spectra only; lamp spectra assumed similar across habitat types).
  - Lighting and habitat pairings designed to support robust lit vs unlit comparisons across both hedgerow and grass-margin guilds.

## Data use and implications for environmental monitoring
- Provides a standardised, well-documented dataset enabling the assessment of ALAN (artificial light at night) effects on caterpillar abundance, mass, and community composition.
- Supports long-term monitoring and cross-study comparisons due to:
  - Matched-pairs design (lit vs unlit) across two habitats.
  - Consistent sampling methods and timing to reduce phenological bias.
  - Detailed site metadata, including precise light types, intensities, and urban-context metrics.
- Potential for data integration:
  - Combine with broader insect biodiversity datasets, urbanization indices, or lighting regime data to assess synergistic effects on Lepidoptera and larval stages.
  - Data uploaded to portals and used to inform lighting policy, habitat management (hedgerow maintenance), and insect conservation planning.

## Limitations and caveats
- Lux measurements are proxy indicators and may not fully capture ecologically relevant spectral effects for all taxa.
- Spectral data available only for grass margins; assumed similarity for hedgerows may introduce some uncertainty.
- Some 2020 samples could not be retained due to COVID-19 restrictions.
- Taxonomic resolution is based on provisional identifications and may entail broader groupings (taxonomic units).

## References
- Boyes, D. H., Evans, D. M., Fox, R., Parsons, M. S., & Pocock, M. J. O. (2021). Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle. Insect Conservation and Diversity, 167-187.
- Longcore, T. & Rich, C. (2004). Ecological light pollution. Frontiers in Ecology and the Environment, 2, 191-198.
- Maudsley, M., Seeley, B., & Lewis, O. (2002). Spatial distribution patterns of predatory arthropods within an English hedgerow in early winter in relation to habitat variables. Agriculture, Ecosystems & Environment, 89, 77-89.
- Merckx, T. & Van Dyck, H. (2019). Urbanization-driven homogenization is more pronounced and happens at wider spatial scales in nocturnal and mobile flying insects. Global Ecology and Biogeography, 28, 1440-1455.
- Porter, J. (2010). Colour Identification Guide to Caterpillars of the British Isles: (Macrolepidoptera). Apollo Books.
- Staley, J.T. et al. (2016). Little and late: How reduced hedgerow cutting can benefit Lepidoptera. Agriculture, Ecosystems & Environment, 224, 22-28.
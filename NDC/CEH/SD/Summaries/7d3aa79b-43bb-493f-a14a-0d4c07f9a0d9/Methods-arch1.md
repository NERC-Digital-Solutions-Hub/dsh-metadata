# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Aim and scope
- Assess effects of artificial light at night (ALAN) on moth caterpillar communities by comparing lit and unlit transects.
- Use a matched-pairs design across two habitat types (hedgerows and grass margins) to disentangle ALAN from urbanisation effects.
- Build on methods from a prior Science Advances study (2021) to inform understanding of ALAN impacts on Lepidoptera life stages.

## Study design and field sites
- Matched-pairs design with 26 lit–unlit pairs (plus one triplet) across hedgerows and grass margins.
- Pairs selected to have comparable habitat structure, separated by ≥60 m (median 118 m) to isolate lighting effects.
- Site screening involved GIS overlay of county street lights and in-person verification via Google Street View and site visits.
- Lighting treatments reflect regional practice: LED, high-pressure sodium (HPS), and a few low-pressure sodium (LPS) sites (14 HPS, 11 LED, 2 LPS).
- Lit transects had been illuminated by the same treatment for at least five years; all sites verified as fully lit during sampling nights (02:00–04:00).
- Light intensity measured with lux at five points along each transect:
  - Hedgerows: 1.25 m height; lit mean 5.7 lux (range 1.42–15.84).
  - Grass margins: 0.25 m height; lit mean 2.2 lux (range 0.18–7.14).
  - Unlit transects: <0.01 lux (minimum recorded 0.1 lux on overcast nights).
- Spectral data (grass margins only): Ocean Optics spectrometer; LED spectral range with CCT ≈ 2700–4000 K; HPS ≈ 2200 K; LPS ≈ 1800 K.
- Habitat matching criteria included: comparable transect length and microclimate, presence/absence of hedgerow trees within 30 m, vegetation height in grass margins, and avoidance of adjacent high-quality habitats.

## Lighting and spectral data details
- Lighting types: LED, HPS, and a minority of LPS sites.
- Spectral considerations: lux is human-vision based; spectral composition can differ in ecological responses.
- CCT values provided for LED and traditional discharge lamps; spectral data used to contextualize light quality differences between treatments.

## Caterpillar sampling and processing
- Two sampling methods to cover feeding guilds:
  - Hedgerow beating in spring (deciduous woody) for 20 taxonomic units; sampling conducted in May 2019 and April 2020.
  - Grass margins sweep netting in winter for noctuid caterpillars on grasses/herbs.
- Sampling details:
  - Hedgerows: three points per transect (14 m each); methods included drainpipes (for box hedges) and beating trays; instar targeting to represent early and late spring phases.
  - Grass margins: transects aligned with road verges or agricultural margins; sweeps performed after sunset (21:00–06:30) on mild nights (min temp ≥ 6°C).
  - Transect lengths typically ~14 m; occasional adjustments when suitable habitat extended beyond this length.
  - Lit and unlit transects sampled an equal number of times; most sites visited ~4 times; one site updated lighting during the study.
- Caterpillar counts and specimens:
  - Grass margins: 826 caterpillars collected; mean mass ≈ 98 mg (range 0.07–2,240 mg).
  - Hedgerows: 1,021 caterpillars collected; mean mass ≈ 43 mg (range 0.2–866 mg).
  - Included 34 day-flying Lepidoptera; grass margins yielded 16 taxonomic units.
- Taxonomic approach:
  - Provisional identifications by the lead author using literature and online resources; categorised into 20 hedgerow units and 16 grass-margin units (plus miscellaneous groups).
  - Both caterpillar and day-flying species included in analyses due to potential nocturnal larval activity being affected by ALAN.
- Specimen handling:
  - All specimens weighed with precise balance; samples retained at -20°C (except some 2020 samples not stored due to COVID-19 restrictions).
  - Botanical context recorded (dominant hedge species, hedgerow height/width; vegetation height for grass margins).

## Data structure and content
- Main data files:
  - Boyes_et_al_2021_hedgerows_mass.csv (hedgerow caterpillar masses)
  - Boyes_et_al_2021_grass_mass.csv (grass-margin caterpillar masses)
- Field site data:
  - Boyes_et_al_2021_field_sites_data.csv
- Key fields (selected):
  - Visit_ID (grass data only), Site_ID, Treatment (unlit, LED, HPS, LPS)
  - Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince (grass margins)
  - Field-site descriptors: Site_Name, Light_Type, Lit_transect_centroid, coordinates, hedgerow/grass characteristics, transect distances
  - Landscape context: urban area within 100/250/500 m, and radius-based urban metrics (Lit/Unlit comparisons)
- Data collection and management:
  - Standardised forms, Excel-based data capture with dropdowns and validation rules
  - Data entered within 24 hours of field visits; double-checked for errors
  - Data kept in a structured format to enable statistical analyses

## Quality control and limitations
- Matched-pair criteria applied to ensure comparable microhabitats; some exclusions based on hedgerow structure and adjacent habitat quality.
- Sampling conducted on the same nights to minimise temperature-related variation; standardized protocols across sites and years.
- Data integrity measures included automated calculations, unit consistency, and internal checks; most samples stored at -20°C, with some 2020 samples not retained due to lab access constraints.
- Limitations acknowledged:
  - Lux-based measurements may not fully capture ecological light exposure due to spectral differences.
  - Spectral data were limited to grass-margin sites; LED spectral output varied and was not exhaustively calibrated.

## References
- Boyes, D.H., Evans, D.M., Fox, R., Parsons, M.S., & Pocock, M.J.O. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle. Insect Conservation and Diversity, 167-187.
- Longcore, T. & Rich, C. (2004) Ecological light pollution. Frontiers in Ecology and the Environment, 2, 191-198.
- Maudsley, M., Seeley, B., & Lewis, O. (2002) Spatial distribution patterns of predatory arthropods within an English hedgerow in early winter in relation to habitat variables. Agriculture, Ecosystems & Environment, 89, 77-89.
- Merckx, T. & Van Dyck, H. (2019) Urbanization-driven homogenization is more pronounced and happens at wider spatial scales in nocturnal and mobile flying insects. Global Ecology and Biogeography, 28, 1440-1455.
- Porter, J. (2010) Colour Identification Guide to Caterpillars of the British Isles: (Macrolepidoptera). Apollo Books, Stenstrup, Denmark.
- Staley, J.T., et al. (2016) Little and late: How reduced hedgerow cutting can benefit Lepidoptera. Agriculture, Ecosystems & Environment, 224, 22-28.
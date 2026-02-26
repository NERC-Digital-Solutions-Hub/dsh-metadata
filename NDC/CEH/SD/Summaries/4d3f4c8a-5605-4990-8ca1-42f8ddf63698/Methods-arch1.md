# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Purpose and study design
- Data collected to compare caterpillar communities under lit versus unlit street-light areas, using a matched-pairs design.
- Two habitat types: hedgerows and grass margins, each with distinct sampling methods.
- Lighting treatments reflect regional technologies (LED, high-pressure sodium; a few low-pressure sodium sites) and are considered long-term (≥5 years).
- Aim to disentangle effects of artificial light at night (ALAN) from urbanisation; light intensity at multiple heights measured; sampling occurred during unfavourable lunar conditions to reduce confounding timing effects.

## Field sites and lighting treatments
- 26 site pairs (lit vs unlit) plus one triplet; located in Oxfordshire, Buckinghamshire, and Berkshire.
- Pairs are geographically close (median 118 m apart) with identical habitat type and similar microhabitats; strict exclusion criteria applied (hedgerow trees, adjacent high-quality habitat, vegetation height differences).
- Lit transects were continuously illuminated; lighting type within pairs included predominantly LED (LED) and high-pressure sodium (HPS), with 2 low-pressure sodium (LPS) sites.
- Site characteristics recorded to ensure comparability (habitat type, dominant plant species, hedge metrics, mowing, etc.).

## Illumination measurements and spectra
- Light intensity measured with lux meters at five points along each transect: hedgerows at 1.25 m (leaf- and caterpillar-relevant height) and grass margins at 0.25 m.
- Lit hedgerows: mean lux ~5.7; lit grass margins: mean lux ~2.2; unlit transects consistently <0.01 lux.
- Spectral data (grass margins only) via Ocean Optics spectrometer; CCT estimates indicate HPS ~2200 K, LPS ~1800 K, LED ranges 2700–4000 K.
- CCT interpretations noted as indicative; spectral calibration was limited, and spectra were not available for all site types.

## Caterpillar sampling and guilds
- Hedgerow sampling (spring): beatings to target woody-plant feeders; three points per transect, with different beating tools depending on hedge structure; sampling dates aligned to spring foliage phenology (mid-May 2019, mid-April 2020).
- Grass margins sampling (winter): sweep-netting to target nocturnal grass- and herbaceous-feeders; transects walked along road verges or field margins; sampling mostly Dec 2018–Apr 2019.
- Sampling times standardized (within nights, typically 21:00–06:30; nights with minimum temperatures ≥6°C).
- Caterpillars identified to taxonomic units (20 hedge units; 16 grass margin units) with inclusion of 34 day-flying Lepidoptera due to potential nocturnal larval stages.

## Data collected and structure
- Hedge data: Boyes_et_al_2021_hedgerow_counts.csv.
- Grass margin data: Boyes_et_al_2021_grass_counts.csv.
- Field site metadata: Boyes_et_al_2021_field_sites_data.csv.
- Key fields include: Visit_ID, Site_ID, Site_Name, Date, Treatment (Lit/UL; Light Type), time-related fields (Sunset, MinsPastSunset), Temp, TransectOffset, counts of all caterpillars (All_Cats), diurnal and nocturnal categories, distance between transects, urban area metrics (within 100/250/500 m radii), hedge characteristics, and light-illumination measures.

## Quality control and data management
- Matched-pair criteria applied with consistent sampling across lit and unlit transects; all sampling conducted on the same nights to minimize temperature effects.
- Standardized data collection forms and drop-down menus; data entered within 24 hours; double-checked for errors and outliers.
- Data stored in CSVs with explicit documentation; specimen retention: most samples stored at -20°C, with COVID-19 disruptions affecting 2020 handling.

## Limitations and considerations for analysis
- Lux is a human-vision-based unit and may not perfectly reflect ecological perception by moth larvae.
- Spectral data were limited (grass margins only) and no full calibration available; CCT values are approximate.
- Some sites and samples were excluded due to habitat differences (hedgerow trees, adjacent natural features) or missing vegetation comparability.
- COVID-19 restrictions affected the retention of some samples from 2020.

## References
- Boyes, D.H., Evans, D.M., Fox, R., Parsons, M.S., & Pocock, M.J.O. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle. Insect Conservation and Diversity, 167-187.
- Longcore, T. & Rich, C. (2004) Ecological light pollution. Frontiers in Ecology and the Environment, 2, 191-198.
- Maudsley, M., Seeley, B., & Lewis, O. (2002) Spatial distribution patterns of predatory arthropods within an English hedgerow in early winter in relation to habitat variables. Agriculture, Ecosystems & Environment, 89, 77-89.
- Merckx, T. & Van Dyck, H. (2019) Urbanization-driven homogenization is more pronounced and happens at wider spatial scales in nocturnal and mobile flying insects. Global Ecology and Biogeography, 28, 1440-1455.
- Porter, J. (2010) Colour Identification Guide to Caterpillars of the British Isles: Macrolepidoptera. Apollo Books.
- Staley, J.T. et al. (2016) Little and late: How reduced hedgerow cutting can benefit Lepidoptera. Agriculture, Ecosystems & Environment, 224, 22-28.
# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales

## Overview
- Describes data sources, data gathering, and analytical methods used to assemble radionuclide activity concentrations in soils, waters, sediments, and terrestrial biota around England and Wales.
- Aimed at categorising naturally occurring radionuclide data (K, U, Th series) by ICRP reference animals and plants (RAPs) to support assessments of radiation exposure to non-human species.

## ICRP reference animals and plants (RAPs)
- RAPs used for terrestrial ecosystems: Reference Deer, Reference Rat, Reference Duck, Reference Frog, Reference Bee, Reference Earthworm, Reference Pine Tree, Reference Wild Grass.
- For data mapping, “any wild mammal” and specific Deer/Rat data were used where RAP-specific data were lacking.
- Objective: attribute available data to RAPs to facilitate exposure assessments for England and Wales.

## Data sources and availability
- Data sourced from:
  - Grey literature, refereed journals, and in-house databases.
  - RIFE (Radioactivity in Food and the Environment) reports (UK-wide data 1995–2004, including mainly edible biota for humans).
  - CEH (Centre for Ecology & Hydrology) datasets, including analyses of radiocaesium and gamma data.
  - BGS G-BASE geochemical baseline surveys for soils, sediments, and waters (K, U, Th concentrations).
- Data coverage is UK-wide but spatially incomplete and variably available by media (soil, sediment, water) and RAP category.
- Some data are direct RAP-specific; much data are attributed to RAPs using predefined mappings (e.g., Duck → any wild bird; Frog → any amphibian; Bee → any flying insect; Earthworm → any earthworm; Pine Tree → any tree; Wild Grass → grass/herb).

## Sampling and analyses
- When data were scarce, a targeted sampling campaign was undertaken for Duck, Bee, Earthworm, Pine Tree, and Frog, supplemented by existing CEH sample archives.
- Collected materials included:
  - Flying insect composites from Environmental Change Network sites.
  - Lodgepole pine trunk samples.
  - Grey heron liver (CEH archive).
  - Earthworms, rabbits, toads, mallards.
- Wales data were incorporated where available; many Welsh samples were sourced due to limited Welsh datasets.

## Sample preparation and analytical methods
- Pine trunk samples: washed, ashed at 450°C.
- Earthworms: gut evacuation, freeze-dried, homogenised.
- Insects: dried and homogenised.
- Mallards: plucked, GI tract removed; liver analysed separately; carcasses ashed.
- Rabbits: skinned, cleaned, ashed after washing.
- Samples freeze-dried or analysed fresh as required.
- Secular equilibrium assumed between 238U and 234U in biological samples; assumed 232Th series in equilibrium; other decay products not always in equilibrium.
- Gamma spectrometry: hyperpure germanium detectors; 59.5–1836 keV range; 2-day counts; calibration with certified reference solutions (density-dependent efficiency).
- For U and Th: total U and Th measured by ICP-MS after acid digestion (HNO3 with HF) in microwave digestion; detection limits ~10^-2 mg/kg for Th and ~10^-3 mg/kg for U.
- Total U/Th activities derived from total concentrations using standard specific activities; equilibrium assumptions applied where justified.

## Derivation of soil activity concentrations and data harmonisation
- Soil activity concentrations derived from the G-BASE geochemical baseline data (K, U, Th) for England and Wales.
- Normalisation across datasets:
  - Data from different analytical techniques and sample types normalised (levelling between BGS and Wolfson Atlas data) using linear quantile transformation where both datasets overlapped.
  - Bedrock/superficial geology coded (simplified) and used to compute area-weighted geometric means for 25 km2 grid squares.
  - For soils and sediments: two approaches per grid square:
    - Geometric means from measured samples (5 × 5 km nearest data points per square).
    - Extrapolated surfaces for areas lacking direct measurements, based on bedrock/geology relationships.
  - For waters: geometric means derived where data existed; extrapolation not applied due to weaker geology-water element relationships.
- Concentrations converted to activity concentrations (K-40, 238U, 232Th) using standard activities; assumed secular equilibrium for 232Th series; 238U chain treatments recognised that equilibrium with subsequent decay products may vary.

## Data structure, metadata and documentation
- Terrestrial biota data are organised by RAP with a metadata-led spreadsheet structure:
  - Species_name, Latin_name, RAP, Use_in_wholebody_calculations_Y, Easting/Northing, Sampling_location, Sampling_date.
  - Activity concentrations by radionuclide (K-40, 238U, 232Th), with detection limits and standard deviations where reported.
  - Tissue_sampled, Reference, Sample_number, Tissue/organ, and any data manipulation notes (Comments).
  - Analysis code and internal CEH identifiers.
- References section lists sources for terrestrial biota and sampling datasets.

## Temporal and geographic coverage
- Biota data: sampling results gathered from 1995–2004 (RIFE period) and CEH archives; some Welsh samples extend the temporal window.
- G-BASE soil/sediment data: long-running geochemical baseline coverage across England and Wales, with variable density (about 1–2 km2 sampling density for soils; similar for sediments).

## Limitations and challenges for data stewardship
- Incomplete RAP-specific data and reliance on indirect RAP mappings for many species.
- Uneven UK coverage and greater data availability for soils and sediments than for waters or certain biota.
- Temporal gaps and methodological changes across datasets requiring normalisation and careful provenance tracking.
- Assumptions of secular equilibrium (232Th, 238U) may not hold for all biota due to differing ecological processes.
- Extrapolation of data to grid squares introduces uncertainty, particularly where direct measurements are lacking.
- Need to document all data transformations, normalisations, and assumptions to maintain reproducibility and traceability.

## Practical implications for data governance
- Provenance and lineage: track origins from RIFE, CEH, and BGS G-BASE, including sampling dates, methods, and locations.
- Metadata standards: store comprehensive metadata for RAP assignment, tissue type, sampling methods, analytical techniques, units (Bq/kg FW for activities; mg/kg FW for total U/Th), LODs, and quality flags.
- Data harmonisation rules: maintain explicit normalisation and extrapolation procedures (quantile transforms, area-weighted means, bedrock/ geology attribution).
- Uncertainty management: capture and communicate uncertainties arising from non-equilibrium assumptions, censored data, and extrapolations.
- Accessibility and reuse: provide clear references, data tables, and methodological details to enable reuse for exposure assessments and cross-study comparisons.

## References (selected)
- Johnson C.C. and Breward N., G-BASE: Geochemical Baseline Survey of the Environment. BGS Report CR/04/016 (2004).
- Johnson C.C., Breward N., Ander E.L. and Ault L., 2005. Geochem.: Explor.-Environ.-Anal., 5(2005) 347-357.
- Beresford N.A. et al., Assessment of naturally occurring radionuclides around England and Wales. Project SC030283 (Environment Agency, 2007).
- Webb J.S. et al., Geochemical Atlas of England and Wales (Wolfson Atlas data integration).
# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Comparative study of moth caterpillar communities under lit vs unlit street sections in two habitats: hedgerows and grass margins.
- Matched-pairs design: 26 lit–unlit pairs plus one triplet; lit vs unlit transects separated by at least 60 m.
- Lighting treatments reflect regional practice: LED, high-pressure sodium (HPS), and two low-pressure sodium (LPS) sites; lit sections had at least five years of the same treatment.
- Two sampling guilds: hedge-beaten caterpillars (spring) and grass-margin sweep-net caterpillars (winter).
- Data are organized into CSV files with rich metadata to enable cross-site comparisons and re-use.

## Field sites and study design
- Sites: contiguous, linear strips of habitat; lit and unlit portions paired geographically close (median 118 m, range 60–527 m).
- Matching criteria ensured comparable habitat features (e.g., hedgerow trees, vegetation structure, surrounding land use) to isolate ALAN effects.
- Sampling methods matched to habitat type:
  - Hedgerows: beating in spring; transects 14 m long with multiple sampling points.
  - Grass margins: sweep-net sampling in winter; transects typically 14 m long.
- Spectral and intensity characterization:
  - Light intensity measured at five points along each transect (lux) at heights corresponding to caterpillar exposure.
  - Spectral data gathered for grass margins; CCT values estimated for LED and HPS/LPS lamps.
- Timing:
  - Fieldwork conducted during the late spring for hedgerows and winter for grass margins; nights between 02:00–04:00 to verify lighting conditions.
  - Mild nights (minimum temperature ≥ 6°C) targeted for caterpillar sampling.
- Data capture:
  - Extensive site-screening and in-person checks to confirm matching criteria before inclusion.

## Lighting treatments
- Lighting types on lit transects: LED, HPS, LPS.
- History: lighting treatments consistently applied for at least five years prior to sampling.
- Night lighting status: fully lit throughout the night; no part-night lighting or dimming detected during visits.

## Caterpillar sampling and measurements
- Hedge sampling (spring): day-time beating along three points per transect; methods include drainpipes for box hedges and beating trays for overhanging vegetation.
- Grass-margin sampling (winter): nocturnal sweeps with a 50 cm diameter net; standardized figure-of-eight motion.
- Sampling frequency:
  - Hedge: two visits per site (May 2019 and April 2020) with 1021 caterpillars recorded.
  - Grass margins: multiple visits from Dec 2018 to Apr 2019; 826 caterpillars recorded.
- Data collected per caterpillar:
  - Mass (mg) with high-precision balance.
  - provisional taxonomic identifications; 20 hedgerow units and 16 grass-margin units; 34 day-flying Lepidoptera included due to potential nocturnal larval influence.
- Post-collection handling:
  - Specimens retained (except spring 2020 due to COVID-19 lab access restrictions) and stored at -20°C where possible.
  - Identifications performed by lead author using literature and ukleps.org.

## Data structure and files
- Main hedgerow data: Boyes_et_al_2021_hedgerows_mass.csv
- Main grass-margin data: Boyes_et_al_2021_grass_mass.csv
- Field site metadata: Boyes_et_al_2021_field_sites_data.csv
- Key columns (examples):
  - Visit_ID, Site_ID, Treatment, Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince (grass margins)
  - Old_Site_ID, SiteID_Fig, Sampling_meth, Site_Name, Light_Type, Lit_transect_centroid/E/N/Lat/Long, Unlit_transect_centroid/E/N/Lat/Long
  - Hedgerow/Grass_mean_illumination, Dist_between_trans, Urban-coverage metrics (100/250/500 m radii)
- Metadata and units:
  - Light intensity (lux) measured at relevant heights (hedgerows: 1.25 m; grass margins: 0.25 m)
  - Spectral data for grass margins; CCT values (LED ~2700–4000 K; HPS ~2200 K; LPS ~1800 K)

## Data quality and processing
- Data collection and entry standardized:
  - Standardised forms and Excel-based spreadsheet with dropdowns; data entered within 24 hours of field visits.
  - Automated calculations via Excel formulas; post-entry double-checks for errors and outliers.
- Quality control limitations:
  - Some samples from spring 2020 not kept due to COVID-19 restrictions.
  - Spectral measurements uncalibrated; CCT estimates are relative values.
- Site matching and sampling consistency:
  - Twenty-six site pairs (plus one triplet) were selected using GIS overlays and virtual/site visits to ensure habitat comparability.
  - Sampling trips were coordinated to keep methods and timing consistent across lit and unlit transects.

## References and context
- Core methodological references cited for ALAN effects and sampling techniques, supporting interpretation of results and replication:
  - Studies on light pollution impacts on moths and related methodologies (e.g., Boyes et al., 2021; Longcore & Rich, 2004; Maudsley et al., 2002; Merckx & Van Dyck, 2019; Porter, 2010; Staley et al., 2016).

## Reuse and potential analyses
- The dataset enables assessment of ALAN effects on larval moth communities across habitat types, with:
  - Direct comparison of caterpillar abundance/mass between lit vs unlit transects.
  - Exploration of how lux levels and spectral properties relate to caterpillar metrics.
  - Evaluation of long-term lighting-type effects using paired-site design, while controlling for vegetation structure and urbanization.
- Rich metadata supports cross-site normalization, spatial analyses, and integration with external urbanization and habitat datasets.
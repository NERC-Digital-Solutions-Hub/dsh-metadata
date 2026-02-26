# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Objective: assess how street lighting (ALAN) influences local moth caterpillar communities across two habitat types (hedgerows and grass margins) using a matched-pairs design.
- Scope: field-based study in Oxfordshire, UK, comparing lit versus unlit transects with long-standing lighting treatments (LED, HPS, LPS) to infer long-term effects.

## Study design and aims for monitoring frameworks
- Matched-pairs approach: 26 lit/unlit site pairs (plus one triplet) where habitat and transect length are matched to isolate ALAN effects.
- Temporal and spatial matching: transects are geographically close (median 118 m apart), aligned along straight roads to minimize microclimatic variation; sampling conducted during consistent nights to reduce temperature effects.
- Long-term exposure: lit transects had the same lighting treatment for at least five years prior to sampling, enabling robust inference about chronic ALAN impacts.
- Habitat controls: exclusion of sites with differing hedgerow trees, adjacent high-quality habitat, or significant vegetation management differences to reduce confounding factors.

## Field sites and lighting treatments
- Habitat types: hedgerows (beating method) and grass margins (sweep netting).
- Lighting treatments across lit transects: LED, HPS, and a small number of LPS sites.
- Spectral considerations: grass margins had spectral data collected; CCT values estimated (LED: 2700–4000 K; HPS ~2200 K; LPS ~1800 K). Lux readings recorded at multiple heights to reflect caterpillar exposure.
- Urban context: site selection included urbanization measures at multiple radii; proportion of urban area used to assess potential confounding by urbanization.

## Caterpillar sampling and methods
- Sampling windows and methods:
  - Hedgerows: spring beating at three points along each transect; methods included drainpipes or beating trays; sampling timed to align with caterpillar life stages (late spring and early spring visits in 2019–2020).
  - Grass margins: winter/spring sweep-netting for noctuid caterpillars that overwinter on grass stems; sampling conducted after sunset across multiple visits per site.
- Temporal coverage: sampling occurred December 2018–April 2019 (grass margins) and 2019–2020 (hedgerows); fieldwork spanned mild nights with temperatures considered.
- Sample sizes: grass margins yielded 826 caterpillars; hedgerows yielded 1021 caterpillars (late spring). Additional data include 34 day-flying Lepidoptera (from both guilds) integrated into analyses due to potential nocturnal larval stages.
- Taxonomic grouping: caterpillars were provisionally identified and grouped into 20 hedgerow taxonomic units and 16 grass-margin taxonomic units; some day-flying species included despite diurnal adults.

## Data collection, quality control, and governance
- Data capture: standardized forms and Excel-based spreadsheets with dropdowns to minimize entry errors; data entry completed within 24 hours of field visits; automated calculations within Excel.
- Verification: records double-checked for errors and outliers; samples stored at -20°C (except some 2020 spring samples due to COVID-19 lab access restrictions).
- Matching criteria enforcement: strict criteria to ensure lit and unlit transects were comparable (vegetation height, dominant plant species where possible, distance between transects, timing, and habitat integrity).
- Metadata and data structure: detailed data dictionaries accompany main data (hedgerow and grass-margin counts) and a field-sites dataset describing sampling methods, light types, transect centroids, illumination means, and urban context radii.
- Data availability and sharing: data are organized for transparency and reuse, with explicit field-site and measurement metadata; references to supporting literature and data lineage provided.
- Limitations and caveats: lux is a human-vision-based measure and may not perfectly reflect caterpillar perception; spectral data were only available for grass margins; some data (e.g., early-spring samples from 2020) were not retained due to COVID-19 restrictions.

## Data structure and key variables
- Main data files:
  - Boyes_et_al_2021_hedgerow_counts.csv: hedgerow caterpillar counts with accompanying metadata per visit.
  - Boyes_et_al_2021_grass_counts.csv: grass margin caterpillar counts with accompanying metadata per visit.
- Field sites data:
  - Boyes_et_al_2021_field_sites_data.csv: site-level information including sampling method (Grass margin, Hedgerow, or both), light type, transect centroids (lit and unlit), mean illumination values, transect distances, urban metrics at 100/250/500 m radii, and related spatial data.
- Example and descriptive fields:
  - Visit_ID, Site_ID, Site_Name, Date, Treatment_1 (Lit/Unlit), Treatment_2 (LED/HPS/LPS/Unlit), MinsPastSunset, Temp_Degree_Celsius, Dist_between_trans, p100/p250/p500 urban metrics, Hedge_Height, Dom_plant_species.
- Data provenance: references to data sources and study practices; alignment with prior literature on street lighting and insect populations.

## Key references and context
- Primary related study: Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle (Boyes et al., 2021).
- Foundational methodological references: Ecological light pollution (Longcore & Rich, 2004); habitat and arthropod distribution studies (Maudsley et al., 2002; Staley et al., 2016); urbanization effects on nocturnal insects (Merckx & Van Dyck, 2019).

## Practical implications for monitoring frameworks
- Demonstrates how to design a robust monitoring program that isolates ALAN effects through matched-pair habitat comparisons and long-term lighting stability.
- Highlights the importance of comprehensive metadata (lighting type, spectral characteristics, lux measurements, habitat descriptors, and urban context) to support data interoperability and governance.
- Shows rigorous quality control and data management practices (standardized forms, versioned datasets, documentation of data restrictions due to external factors like pandemics).
- Provides a ready-to-use data structure for ecological monitoring datasets, enabling analyses of ALAN impacts on larval Lepidoptera across habitats and lighting treatments.
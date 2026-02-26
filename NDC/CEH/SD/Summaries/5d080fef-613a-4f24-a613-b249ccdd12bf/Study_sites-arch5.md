# Study sites

## Overview
- Three 50 x 50 m plots near Andasibe village, Corridor Ankeniheny-Zahamena (CAZ), eastern Madagascar.
- Plots represent different land-use histories:
  - Forest (Semi-mature forest, SMF)
  - Reforested tree fallow (Young secondary forest, YSF)
  - Degraded land (Degraded grassland, DL)
- Data describe site characteristics and key vegetation metrics collected over a one-year study period.

## Site characteristics by plot

- Forest (SMF)
  - Elevation: 950 m above mean sea level
  - Coordinates: Latitude 18.9317 S, Longitude 48.4117 E
  - Aspect: NE (80°)
  - Average slope: 18°
  - Diameter at Breast Height (DBH): 9.3 cm (±4)
  - Basal area: 35.5 m² ha⁻¹
  - Stem density: 5233 stems ha⁻¹
  - Average canopy height: 19 cm (±8.0)
  - Leaf Area Index (LAI): 3.39 (range 3.11–3.58)
  - Dominant species: Abarahania ditimena, Brachulaena ramiflora, Cryptocaria spp., Ocotea samosa, Eugenia sp., Leptolaena
  - Land-use history: Forest resprouted after selective illegal logging ceased in 1995; protected forest managed by Mitsinjo Association; majority trees ~20 years old as of Oct 2014; remnant trees present

- Reforested tree fallow (YSF)
  - Elevation: 990 m above mean sea level
  - Coordinates: Latitude 18.9472 S, Longitude 48.3953 E
  - Aspect: NW (350°)
  - Average slope: 16°
  - DBH: 6.1 cm (±1.3)
  - Basal area: 6.3 m² ha⁻¹
  - Stem density: 2133 stems ha⁻¹
  - Average canopy height: 5 cm (±0.31)
  - LAI: 1.83 (1.75–2.14)
  - Dominant species: Primarily Psiadia altissima (95% of stems), with few Cassinopsis madagascariensis and Harungana madagascariensis (<5%)
  - Land-use history: Cut and burned for rice cultivation in 1990; ~10 years of slash-and-burn; no slash-and-burn since 2000; forest restoration program since 2000; native species introduced but largely outcompeted by Psiadia altissima

- Degraded land (DL)
  - Elevation: 970 m above mean sea level
  - Coordinates: Latitude 18.9462 S, Longitude 48.4069 E
  - Aspect: NE (80°)
  - Average slope: 17°
  - DBH: data not available
  - Basal area: data not available
  - Stem density: data not available
  - Average canopy height: data not available
  - LAI: data not available
  - Dominant species: Imperata cylindrica, Helichrysum sp., Lodetia sp.
  - Land-use history: Degraded land abandoned in 2000 after ~15 years of slash-and-burn

## Data quality, gaps, and time frame
- One-year study period; LAI reported as a mean with range for the forest plots
- Several parameters missing for the Degraded land plot (and some structural metrics not reported for all plots)

## Data governance and sharing considerations
- Ensure precise plot-level metadata: plot_id, coordinates, elevation, aspect, slope
- Record measurement details for each metric (units, methods, date range)
- Capture land-use history and management context (e.g., NGO involvement, restoration interventions)
- Document data collectors and QA steps; establish clear licensing and access terms
- Plan for uploading to relevant data portals and catalogues; update with new data as sites continue to change

## Suggested metadata fields for stewardship
- Project and site_id
- Geographic: coordinates (lat, lon), elevation, aspect, slope
- Vegetation metrics: DBH_mean, DBH_sd, basal_area, stem_density, canopy_height_mean, canopy_height_sd, LAI_mean, LAI_range
- Ecology: dominant_species_list
- Land_use_history and management actions
- Temporal: data_collection_period, measurement_methods
- Provenance: data_collector, QA_steps, data_source, data_format, license
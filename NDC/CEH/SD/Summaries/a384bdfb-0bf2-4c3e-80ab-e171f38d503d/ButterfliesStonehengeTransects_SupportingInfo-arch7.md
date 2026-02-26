# Stonehenge Landscape Lepidoptera 2010-2011

## Overview
- Compilation of raw data on the behavior and distribution of Lepidoptera (butterflies and day-flying moths) at the Stonehenge Landscape during 2010-2011.
- Includes Lepidoptera survey data and botanical data (flowering units and percent cover in quadrats).
- Data quality assurance performed to identify outliers and anomalies, with exploratory analysis referenced.

## Study area
- Location: National Trust Stonehenge Landscape within the Stonehenge World Heritage Site, Wiltshire, SW UK.
- Context: Long-term landscape-scale grassland restoration (2000-2012) to protect archaeological features and restore ecological value.
- Habitat mosaic: Chalk grassland fragments on slopes and barrows, grassland restoration fields of varying ages, semi-improved pasture, arable land, and woodland.

## Data collection methods (Lepidoptera surveys)
- Survey method: Transect surveys adapted from the Butterfly Monitoring Scheme (Pollard & Yates, 1993).
- Procedure: Walk transect at a steady pace; record Lepidoptera observed within 5 m of the transect and ahead; nectar plant if feeding.
- Timing and layout:
  - 2010: 17 transects, each 200 m long; conducted on three occasions during June–September; habitats included older and newer grassland recreation, arable land, chalk fragments, barrows, and semi-improved pasture.
  - 2011: 120 m transects with location and side (West/East) details, sheltered or exposed, grid references provided.
- Data captured per observation: species, sex (where noted), date, start/end times, transect code, transect segment (20 m), replicate, weather (temperature, wind, cloud cover), behavior (flying, nectaring, dispute, courting, mating, basking, resting), and totals.

## Habitat quality measurements
- Vegetation and nectar resources quantified along each transect.
- Methods:
  - Five habitat transects and four matrix transects per survey.
  - Quadrat sampling within 20 m segments to measure vegetation height/density, bare ground, and dead vegetation.
  - Nectar resources quantified by flowering units and their taxonomic families (Dipsacaceae, Fabaceae, Asteraceae).
- Weather data: hourly conditions from Boscombe Down meteorological station (6.5 km away).

## Data organization and GIS-ready structure
- Primary datasets (sheets) and their contents:
  - Lepidoptera 2010: Transect-level Lepidoptera counts and behaviors; 2010 data structure with species codes and observation details.
  - Resources 2010: Habitat resources and nectar plant data corresponding to 2010 transects.
  - Lepidoptera 2011: Location-based transect data for 2011 (120 m transects); location codes, side of fragment, sheltered/exposed, and grid references.
  - Resources 2011: Resource measurements for 2011 transects, including drop disc, bare ground, dead vegetation, nectar, and family-level nectar breakdown.
- Spatial references and GIS attributes:
  - Transects linked to start/end grid references (SU) and British National Grid (BNG).
  - Transect lengths provided (e.g., 200 m for many 2010 transects; 120 m for 2011 transects; multiple locations with precise grid references).
  - Location codes and habitat types (e.g., Chalk fragments, restorable grasslands, arable) to enable map-layer categorization.
  - Tables include species codes and taxonomic/nomenclature mappings for Lepidoptera and flowering plants (standard references cited).

## Taxonomy and nomenclature
- Lepidoptera: Standard British references used for species names and codes (e.g., Forester, Small Tortoiseshell, Green-veined White, Common Blue, etc.), with a defined species code system.
- Plants: Nomenclature follows Stace (2010) and associated floras; flowering plant species listed with common names and codes to support nectar-resource mapping.

## Data fields and quality considerations
- Lepidoptera data fields: date, transect, segment, replicate, temperature, wind, cloud cover, species code, sex, nectaring, and various behavioral states (dispute, courting, mating, basking, resting), plus totals.
- Resources data fields: date, transect, segment, drop disc, bare ground, dead vegetation, total flowering units, nectar totals, and family-level breakdown (Asteraceae, Fabaceae, Dipsacaceae).
- 2010 and 2011 datasets provide comprehensive ties between Lepidoptera observations and corresponding habitat/nectar-resource measurements.
- Data quality: Outliers and anomalies were checked using species occurrence expectations and exploratory analysis; some datasets note ad-hoc survey timing to minimize temporal and diurnal effects.

## Data sources and references
- Methodological basis: Pollard & Yates (1993) transect method; vegetation and nectar measurement methods cited (Stewart et al. 2001; Hardy et al. 2007; Carvell 2002).
- Nomenclature references for plants and Lepidoptera: Stace (2010), Langmaid et al. (1989), Heath & Emmet (1985).
- Site management and landscape context: Stonehenge World Heritage Site Management Plan (Young et al., 2009).

## How GIS specialists can use this data
- Create map layers for transect lines (2010 and 2011) with attributes: location code, habitat type, transect length, side of fragment, sheltered/exposed, grid references.
- Build species distribution maps using transect-level counts and species codes; integrate with nectar-resource maps (flowering units by plant species and family).
- Develop habitat-quality maps by integrating vegetation density, bare ground, and nectar resources along transects.
- Enable temporal comparisons (2010 vs. 2011) and cross-reference with weather conditions to assess spatial patterns and habitat associations.
- Use standard nomenclature tables to join Lepidoptera and flowering plant data for richer GIS-driven analyses and visualization.
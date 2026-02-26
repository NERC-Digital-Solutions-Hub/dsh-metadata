# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

## Overview
- Provides supporting documentation for the ECN Cairngorm spider dataset.
- Spiders collected from pitfall traps in three habitats (pine woodland, wind-clipped heath, bog) within the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- Data collected using standard ECN protocol; specimens identified by a single expert araneologist for consistency.
- Related methods and temporal trends discussed in a 2020 report (Andrews et al.) available online; provincial protocols available at ECN.

## Location and study sites
- Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
  - Coordinates: 57° 6' 28"N, 3° 50' 6"W.
  - Elevation range: 320 m to 1111 m above sea level; area ≈ 10 km².
  - Focused transect sampling on west-facing slopes north of the catchment; three habitats at 460–690 m a.s.l.
- Habitats:
  - Woodland transect: 460 m a.s.l., mature Scots Pine with Vaccinium myrtillus dominating understory.
  - Heath transect: 690 m a.s.l., wind-clipped Calluna-Cladonia dry heath with bare ground patches.
  - Bog habitat: 690 m a.s.l., blanket mire with Eriophorum vaginatum and Molinia caerulea.

## Sampling protocol
- Habitat-specific transects: 100 m each with 10 pitfall traps at 10 m intervals.
- Trap details: polypropylene pots (75 mm × 105 mm), buried flush with ground, filled with ethylene glycol to 30 mm depth; galvanized wire mesh (~20 mm square) to exclude small vertebrates; 140 mm plastic rain cover with ~30 mm gap to ground.
- Sampling cadence: fortnightly from roughly April to end October, start date depending on snow-free conditions.
- Specimen handling: samples aggregated by habitat; all specimens identified to species and sex by the same expert araneologist; stored at UKCEH Edinburgh for future research.

## Data structure and units
- Format: long-format CSV.
- Key fields:
  - Year (YYYY)
  - Date (DD/MM/YYYY)
  - Month (MMM)
  - Week (two-digit)
  - Habitat (Bog, Heath, Wood)
  - Transect (e.g., T1)
  - Transect age (Old = pre-2007, New = post-2007)
  - Family (taxonomic family, e.g., Linyphiidae)
  - Species (full species name)
  - Male (count)
  - Female (count)
  - Total (Male + Female)
- Purpose: records counts of spider individuals by species, sex, transect, habitat, and time.

## Quality control and limitations
- Transects relocated after 2007; data spanning pre- and post-relocation should be treated cautiously as a long-term dataset.
- 2007–2008 overlapped both old and new transects to aid transition.
- Data labelled to indicate transect origin (old vs. new).
- Annual sampling periods vary due to weather, snow, and technical issues; typical window is April to November on a biweekly basis, but not guaranteed.
- Standardization recommendation: compute spider counts using the time between first and last trapping date rather than relying on sampling effort alone, as actual effort can vary.

## Data use and GIS considerations
- Suitable for map-based visualization by habitat, transect, and year.
- When aggregating across years, account for transect relocation (pre- vs post-2007) to avoid biases in long-term trend analyses.
- Can be joined with ECN protocols for reproducibility and cross-site comparisons.

## References
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. Wallingford, UK Centre for Ecology & Hydrology. http://nora.nerc.ac.uk/id/eprint/528208
- Protocols: http://www.ecn.ac.uk/measurements/terrestrial/i/ia
- Related dataset reporting: http://nora.nerc.ac.uk/id/eprint/529051/
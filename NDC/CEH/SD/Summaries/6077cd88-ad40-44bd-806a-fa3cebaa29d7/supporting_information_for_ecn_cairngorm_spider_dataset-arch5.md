# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

- Purpose and scope
  - Provides supporting documentation for the ECN Cairngorm spider dataset (2004–2021).
  - Spiders collected from three habitats (pine woodland, wind-clipped heath, bog) within the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
  - All specimens identified by a single expert araneologist to ensure consistency.
  - Related methods and temporal diversity analysis reported in Andrews et al. (2020).

- Location and study area
  - Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (approx. 57°6'28"N, 3°50'6"W).
  - Elevation: 320–1111 m a.s.l., area ~10 km².
  - Focused transects on west-facing slopes (460–690 m a.s.l.) across three habitats:
    - Woodland transect at ~460 m a.s.l. (mature Scots Pine with Vaccinium myrtillus)
    - Heath transect at ~690 m a.s.l. (wind-clipped dry heath)
    - Bog transect at ~690 m a.s.l. (blanket mire)

- Sampling protocol
  - 100 m transect per habitat, with 10 pitfall traps every 10 m.
  - Trap design: 75 mm × 105 mm polypropylene pots buried flush, filled with ethylene glycol to 30 mm; top mesh to exclude small vertebrates; 140 mm rain cover with ~30 mm ground gap.
  - Sampling frequency: fortnightly from spring to autumn (April to end October), start date depends on snow-free ground.
  - Specimen handling: samples aggregated per habitat; identification to species and sex (from 2006 onwards) by a single expert; all specimens stored at UKCEH Edinburgh for future research.

- Data structure and units
  - Data stored in long CSV format with the following fields:
    - Year (YYYY)
    - Date (DD/MM/YYYY) and Month (MMM)
    - Week (2-digit)
    - Habitat (Bog, Heath, Wood)
    - Transect (e.g., T1) and Transect_age (Old for pre-2007, New for post-2007)
    - Family (taxonomic family)
    - Species (full species name)
    - Male (count, from 2006 onwards)
    - Female (count, from 2006 onwards)
    - Total (male + female)
  - Provides a standardized, programmatic structure suitable for downstream analysis and integration.

- Quality control and data provenance
  - Transects were moved in 2007; two years (2007–2008) included overlap where old and new transects operated concurrently to aid continuity.
  - Data labeled to indicate which transect data belong to (pre- vs post-2007) to aid dataset integrity.
  - Annual sampling duration varies due to weather, snow, or technical issues; standardization recommended using the interval between first and last trapping dates, not merely the number of sampling events.
  - Covid-19 in 2020: sampling between 01 May and 31 July conducted monthly rather than fortnightly; overall duration for cross-year analyses remained unaffected.

- Usage notes and caveats
  - Caution advised when using the full long-term dataset due to transitional changes in transect location and potential inconsistencies across the pre/post-2007 boundary.
  - Trapping effort across years can still be quantified using in-situ trap data, enabling comparability when standardizing by trapping period rather than raw counts alone.
  - The dataset supports analyses of temporal trends in spider communities, with explicit documentation on protocols and data handling to support reproducibility.

- Data access and references
  - Specimens stored at UKCEH Edinburgh; data intended for future research use.
  - Related analysis report: Andrews, C., Snazell, R., Dick, J. (2020) Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007–2019.
  - Protocol details are available at ECN protocol documents.

- Key takeaway for data stewardship
  - This dataset is a largely standardized, longitudinal spider dataset with clear documentation of habitat types, sampling design, identification practices, and data structure.
  - Essential governance considerations include maintaining metadata on transect relocation (pre/post-2007), documenting sampling completeness per year, and preserving specimen storage information to ensure future re-use and reproducibility.
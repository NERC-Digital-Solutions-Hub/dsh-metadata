# Supporting information for the dataset:
UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J.
Sept. 2021

## Overview
- Provides supporting documentation for the ECN Cairngorm spider dataset (2004–2019).
- Spiders collected from three habitats (pine woodland, wind-clipped heath, bog) in the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- Standard ECN protocol used; identifications performed by a single expert araneologist for consistency.
- Data underpin a temporal analysis of spider diversity (see Andrews et al., 2020) and are available for future research.

## Location and Habitats
- Site: Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57° 6' 28" N, 3° 50' 6" W).
- Elevation: Catchment 320–1111 m a.s.l.; study transects focused on west-facing slopes between 460–690 m a.s.l.
- Habitats:
  - I. Woodland transect: ~460 m a.s.l., mature Scots Pine with Vaccinium myrtillus.
  - II. Heath transect: ~690 m a.s.l., wind-clipped Calluna-Cladonia dry heath with bare ground patches.
  - III. Bog habitat: ~690 m a.s.l., blanket mire with Eriophorum vaginatum and Molinia caerulea.

## Sampling Protocol
- Design: In each habitat, a 100 m transect with 10 pitfall traps spaced 10 m apart.
- Trap details: polypropylene pots (75 mm × 105 mm) buried flush with ground; filled with ethylene glycol to 30 mm; top mesh ~20 mm2 to deter small vertebrates; rain covers (140 mm) with ~30 mm ground gap.
- Frequency: Fortnightly sampling from approximately April to end October; start date depends on snow-free ground.
- Processing: Spiders aggregated by habitat per sampling period; all specimens identified to species and sex by the same expert; vouchers stored at UKCEH Edinburgh for future research.

## Data Structure and Units
- Format: Long-format CSV.
- Key fields:
  - Year (YYYY)
  - Date (DD/MM/YYYY)
  - Month (MMM)
  - Week (2-digit)
  - Habitat (Bog, Heath, Wood)
  - Transect (e.g., T1)
  - Transect age (Old = pre-2007, New = post-2007)
  - Family (taxonomic)
  - Species (full binomial)
  - Male (count)
  - Female (count)
  - Total (Male + Female)
- Notes: Data are organized to support species- and sex-specific counts across habitats and transects, with transect age indicating the pre/post-2007 relocation.

## Quality Control and Limitations
- Transect relocation: Sampling transects moved in 2007; results require caution when forming a continuous long-term dataset due to potential spatial inconsistency.
- Overlap year: 2007–2008 included both old and new transects running simultaneously to aid continuity.
- Labeling: Data explicitly labelled to indicate which transect belongs to pre- or post-2007 schemes.
- Sampling variability: Annual sampling periods vary due to snow, weather, and technical issues; typical aim is early April to early November on a two-week basis, but not guaranteed.
- Standardization guidance: When comparing across years, standardize using the time span between first and last trapping dates rather than raw sampling effort. Even with missed dates, traps remain in place and provide continuing sampling opportunity.

## Data Access and References
- Data and methods are described in ECN and related project documents.
- Related analysis: Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007–2019.
- Access to the detailed methods and datasets is available via UKCEH/NORA repository links provided in the documentation.

## Potential Uses for Data Leaders
- Develop time-series analyses of spider diversity across habitat types and transects.
- Assess effects of habitat type and elevation on spider communities, accounting for pre/post-2007 transect relocation.
- Use metadata (transect age, sampling windows, and storage) to improve data governance, provenance, and reuse in cross-site analyses.
- Leverage standardized, long-format structure for reproducible analyses and integration with other ECN datasets.
# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

## Purpose and scope
- Provides documentation for the ECN Cairngorm spider dataset (2004–2021), including methods and temporal trends in spider diversity at the site.
- References to a companion report (Andrews et al., 2020) and ECN protocols for detailed methods.

## Location and study site
- Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- Coordinates: 57°6'28"N, 3°50'6"W; catchment ~10 km²; elevation 320–1111 m.
- Focused transect sampling on west-facing slopes north of the catchment; three habitats sampled (460–690 m a.s.l.).

## Habitats and sampling design
- Habitats:
  - I. Woodland transect (460 m a.s.l.): mature Scots Pine with Vaccinium myrtillus shrubs.
  - II. Heath transect (690 m a.s.l.): wind-clipped Calluna-Cladonia dry heath with bare ground patches.
  - III. Bog habitat (690 m a.s.l.): blanket mire with Eriophorum vaginatum and Molinia caerulea.
- Sampling layout: 100 m transect per habitat with 10 pitfall traps at 10 m intervals.
- Pitfall trap details: polypropylene pots (75 mm × 105 mm) buried flush; filled with ethylene glycol to 30 mm; 20 mm² mesh to exclude small vertebrates; 140 mm rain cover with ~30 mm ground gap.
- Sampling frequency: fortnightly from ~April to end October, start date depends on snow-free ground.
- Specimen handling: specimens identified to species and sex (from 2006 onward) by the same araneologist; stored at UKCEH Edinburgh.

## Data collection and processing
- Each sampling event yields a single sample per habitat; all spiders from the duration were identified.
- Data and methods aligned with ECN protocols; related data analyses documented in the 2020 report.
- Data stored at UKCEH Edinburgh for future research.

## Data structure and units
- Long-format CSV with fields:
  - Year (YYYY)
  - Date (DD/MM/YYYY)
  - Month (MMM)
  - Week (two-digit)
  - Habitat (Bog, Heath, Wood)
  - Transect (e.g., T1)
  - Transect_age (Old = pre-2007, New = post-2007)
  - Family (taxonomic family, e.g., Linyphiidae)
  - Species (full species name, e.g., Hilaira frigida)
  - Male (count; from 2006 onward)
  - Female (count; from 2006 onward)
  - Total (Male + Female)
- Data represent counts of specimens by species per habitat and transect per sampling event.

## Quality control and caveats
- Transects relocated after 2007; two-year overlap (2007–2008) with old and new transects to maintain continuity.
- Data labeling indicates which transect data belong to old vs. new setups.
- Sampling periods vary due to weather; standardization advised by using the time span between first and last trapping date rather than sampling effort.
- Traps remain in situ even if collection dates are missed; trapping effort can still be estimated across the year.
- 2020 Covid-19 adjustments: 01 May–31 July sampling reduced to monthly rather than fortnightly; overall between-year analysis duration unaffected.

## References and related documentation
- Andrews, C., Sanzell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007–2019: data analysis report. UKCEH.
- Protocols reference: ECN Protocols IA.pdf (ecn.ac.uk).
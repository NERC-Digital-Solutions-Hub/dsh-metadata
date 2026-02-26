# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

- Objective
  - Investigate how organic matter (leaf litter) addition affects cellulolytic decomposition in headwater streams.
  - Use tensile strength of calico strips as a proxy for decomposition rates, enabling calculation of percent loss relative to controls.

- Experimental design and sampling regime
  - BACI design: each stream has an upstream reference zone and a downstream experimental zone, with 20–50 m separation to maintain independence.
  - Time periods:
    - Before period (T1): 61–65 days from early Nov 2012 to early Jan 2013; no manipulation; both zones treated equally.
    - After period (T2): 57–62 days from early Jan 2013 to Mar 2013; experimental zone receives leaf litter addition.
  - Leaf litter addition:
    - One-tonne bags (oak, birch, alder) added to the experimental zone at T2, proportional to zone area, to maintain natural senescence input.
    - Vegetable nets ensure a minimum wet weight of 1.7 kg/m² in the experimental zone.
    - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after two storm events.
  - Locations and replication:
    - Six experimental units (cotton strips) placed randomly per reach in the experimental zones.
    - For each stream, a reference (control) zone is maintained upstream of the experimental zone.

- Data collection and laboratory analysis
  - Field collection:
    - Cotton strips collected at the end of T1 and T2, then frozen at -20°C.
  - Laboratory processing:
    - Strips rinsed, oven-dried to constant mass at 65°C.
    - Tensile strength measured with a Hounsfield machine (25 kN load cell, 40 mm test gap); one estimate of breaking strain per strip.
    - Three untreated strips per batch monitored as controls for transport and washing effects.
  - Data generated per strip:
    - Breaking_strain (Newtons)
    - %_loss (percent loss of tensile strength relative to control batch)

- Data structure and variables
  - Data files are flatbed CSV with 10 columns:
    - site_code: sampling site identifier
    - region: stream basin region
    - date: sampling date
    - time: Before or After manipulation (T1 or T2)
    - landuse: basin land-use
    - reach: Experimental or Control site
    - replicate: replicate code (A–F for six replicates)
    - exposure: days exposed
    - breaking_strain: tensile strength (Newtons)
    - %_loss: percent loss of tensile strength versus control

- Supporting and provenance information
  - Miscellaneous supporting document: DURESS_CU_site_description.csv (site descriptions with coordinates and other metadata)
  - References cited for context and methods:
    - Hladyz et al. 2011
    - Layer et al. 2010
    - Jenkins, Woodward & Hildrew 2013
  - Data references:
    - Links to related sources may be found via the CEH Data Catalogue Record (link permanence not guaranteed)

- Quality control and calibration
  - Calibration: None documented
  - Quality control: None documented; control strips used to account for non-manipulation-related strength loss during transport and washing
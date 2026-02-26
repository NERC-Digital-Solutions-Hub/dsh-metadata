# Supporting documentation on the patch-discovery experiment

- Objective
  - Examine how changes in local population density influence the discovery of a novel food resource by three bird species (great tits, blue tits, marsh tits).

- Study setting and subjects
  - Location: Wytham Woods, Oxfordshire, UK (51°46′N, 1°20′W).
  - Species: great tit (Parus major), blue tit (Cyanistes caeruleus), marsh tit (Poecile palustris).
  - Methods: birds trapped in winter with mist-nets or spring in nestboxes; fitted with a unique BTO metal ring and a plastic PIT tag.

- Experimental design
  - Part of an experimental manipulation of local population density (density manipulation described in Supporting documentation_Exp_density).
  - Setup: a novel food patch (new feeder with sunflower seeds) placed next to each of the two existing feeders (≈40 m apart) at experimental and control sites; novel feeders placed in opposite directions within each site.
  - Second patch-discovery experiment: other locations selected during the density manipulation.
  - Novel feeders: same design as existing ones to avoid neophobia; accessible to all PIT-tagged birds.
  - Deployment timing: set up either the day before the experiment after sunset or on the day of the experiment before sunrise; feeders in place for one day.

- Data collection and dataset structure
  - Data collectors: Keith McMahon, Sam Croft, Kristina Beck.
  - Dataset: one CSV file recording each individual visit to a novel feeder, with fields:
    - Date and time of visit
    - Logger (novel feeder identifier)
    - Site (experimental or control location)
    - Species code (Bto.species.code; greti = great tit, bluti = blue tit, marti = marsh tit)
    - Individual identity (Bto.ring)

- Variables and codes
  - Bto.ring: individual bird identifier (PIT-tagged)
  - Site: experimental vs. control location
  - Bto.species.code: greti, bluti, marti

- Timeline
  - January–March 2021
  - Periods before and during the density manipulation

- References
  - Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.
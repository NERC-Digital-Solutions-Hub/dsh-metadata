# Amazon Fertilization Experiment (AFEX)

## Study area and context
- Located within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
- Humid tropical climate: mean ~26.7°C; ~2200 mm annual precipitation; distinct dry season (Jul–Sep) and peak rainfall (Mar–Apr).
- Dense Terra Firme rainforest; canopy 30–37 m (emergents to 55 m); red-yellow podzolic and latosol soils with high weathering, acidity, and low fertility.

## Experimental design and plot layout
- AFEX is a full factorial fertilization experiment started in March 2017.
- Treatments: seven fertilizer treatments plus a control, yielding eight treatment combinations:
  - N, P, and cations (K, Ca, Mg) individually and in combinations: N+P, N+CATIONS, P+CATIONS, N+P+CATIONS.
- Structure: 32 plots total, with four replicates per treatment, arranged in four independent blocks spaced at least 250 m apart.
- Plot dimensions: each plot 50 x 50 m; treatments applied annually in three applications to reduce leaching/runoff.
- Plot delineation (AFEX 2.0): annual fertilization roadmap with three applications; fertilizers manually distributed along a systematic walk.

## Seedling sampling protocol
- Within each 50 x 50 m plot, a nested 30 x 30 m sampling area contains four 1 x 1 m subplots; across the entire study, this yields 16 subplots per treatment and 128 subplots in total (4 blocks x 4 subplots per block x 8 treatments = 128).
- In each 1 x 1 m subplot:
  - All plant individuals taller than 20 cm and with diameter at ground height (DGH) < 1 cm identified and tagged; palms and lianas not sampled.
  - For each sampled individual, the closest 10 mature leaves to the apical yolk are marked and monitored biweekly for herbivory assessment.
- Leaf-level herbivory assessment:
  - Visual percent leaf area loss evaluated using a standardized method (Johnson et al. 2016), with sectoring and a millimeter grid to improve accuracy.
  - Additional data collected: gall presence (GAIL), fungus presence (FUNGUS), leaf miners presence (LEAF_MINERS) at the leaf level; leaf-injury data collected bimonthly over 12 months, across six campaigns (four in the rainy season, two in the dry season).

## Data file structure and key variables
- Data file: seedlings_herbivory.csv
- Size: 27,510 rows, 14 columns.
- Columns (sample description):
  - A CENSUS: Sampling number
  - B MONTH: Month of sampling
  - C DATE: Sampling day
  - D TRT: Plot treatment (reference to AFEX treatments)
  - E BLOCK: Block number (1–4)
  - F PLOT: Plot within block (1–8)
  - G SUBPLOT: Subplot number (1–4)
  - H INDIVIDUAL: Seedling tag
  - I LEAF: Leaf tag
  - J HERBIVORY: Leaf area loss due to herbivory (percent)
  - K GAIL: Gall presence (1) / absence (0)
  - L FUNGUS: Fungus presence (1) / absence (0)
  - M LEAF_MINERS: Leaf miners presence (1) / absence (0)
  - N MORTALITY: Leaf death (1) / not dead (0)

## Data management, documentation, and sharing
- Data provenance: field protocols for fertilization, plot delineation, and leaf sampling documented; standardized methods for herbivory assessment and leaf-level observations followed.
- Data curation: explicit data dictionary (variable names, meanings, units) and clear coding for categorical/binary fields (e.g., GAIL, FUNGUS, LEAF_MINERS, MORTALITY).
- Documentation practices: consistent naming (seedlings_herbivory.csv) and references to treatment definitions and plot layout.
- Sharing and reuse considerations:
  - Metadata should include study area, plot design, sampling schedule, measurement methods, and data dictionary.
  - Data should be uploaded to relevant portals/catalogs with versioning, licensing, and access details.
  - Potential for re-use in meta-analyses of nutrient addition and herbivory dynamics in tropical forests.

## Data quality considerations, limitations, and challenges
- Exclusion of palms and lianas may limit dataset applicability to all forest seedlings.
- Nested sampling design (multiple subplots within plots) requires careful aggregation and hierarchical analysis to avoid pseudo-replication.
- Seasonal sampling (six campaigns across a year) provides temporal coverage but may still miss atypical events.
- Data integrity relies on manual fertilization and hand distribution, which can introduce procedural variability.
- Data richness at leaf level (presence/absence of various biotic factors) offers detailed insight but requires careful handling of zero-inflated or rare-event variables.

## References
- Chauvel, 1982; Comita et al., 2007; Johnson et al., 2016; Laurance et al., 1999; Lovejoy & Bierregaard, 1990; Quesada et al., 2010, 2011; RADAMBRASIL, 1978; Ranzani, 1980.
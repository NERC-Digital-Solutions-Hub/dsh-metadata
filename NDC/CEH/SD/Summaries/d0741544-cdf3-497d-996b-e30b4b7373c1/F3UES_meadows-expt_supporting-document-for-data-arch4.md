# Supporting document for dataset: Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK

## Overview
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the BESS programme.
- Field-scale manipulation experiments across six urban greenspaces in Bedford and Luton (UK), plus Cranfield University site.
- Objective: quantify how plant floristic diversity and vegetation height affect biodiversity across plants, invertebrates, and soil microbial communities.
- Data linked to a broader study: Norton et al. (2019) Ecological Applications (urban meadows).

## Study design and scope
- Nine meadow treatments formed by all combinations of:
  - Height: Short (H1), Medium (H2), Tall (H3)
  - Diversity: Low (D1), Medium (D2), High (D3)
- Plots:
  - Typical size: 250 m2 (12.5 m x 20 m)
  - Cranfield: 50 m2 plots due to space
  - An unmanipulated control area surveyed at each site
- Establishment and management:
  - Sown May 2013 on clay-loam soils; glyphosate prep; weed management; reseeding if needed
  - Site-specific adjustments (e.g., some plots re-sown, some plots removed or modified due to resident feedback)
- Sites and context:
  - Bedford: Chiltern Avenue, Jubilee Park, Goldington Green, Brickhill Heights
  - Luton: Bramingham Road
  - Cranfield University (rural-urban fringe)
- Data collection years:
  - Botanical surveys in 2014–2015
  - Invertebrate sampling in summer and autumn of year 2, plus winter sampling in 2016 (end of year-2 post-sowing), and Cranfield data in year 3
  - Soil sampling in 2015 for C, N, pH; PLFA analysis; DNA sequencing (ITS/16S)

## Data structure and files (11 CSVs)
- File 1: F3UES_meadows-expt_treatments-plants.csv — links to site, plot, and treatment details; original treatment codes; calendar year and years since sowing.
- File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv — quadrat-level plant data (Domin cover scale); species, whether sown, percent cover.
- File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv — plot-level, observer-based (DAFOR) plant surveys and flowering cover; notes on visibility and zero recordings.
- File 4: F3UES_meadows-expt_inverts_sampling-programme.csv — sampling program identifiers for invertebrate data (sampling method, plots, dates, seasons).
- File 5: F3UES_meadows-expt_inverts_winter.csv — winter invertebrate surveys (taxonomic info and abundances).
- File 6: F3UES_meadows-expt_inverts_visual-surveys.csv — visual invertebrate surveys (observer-based, taxa targets and classification guidance).
- File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv — vacuum and sweep invertebrate samples (taxa, abundances; notes on sampling limitations).
- File 8: F3UES_meadows-expt_inverts_biomass.csv — biomass estimates derived from invertebrate data (dry weight, specimen counts, surrogate weights where needed).
- File 9: F3UES_meadows-expt_inverts_coleoptera.csv — Coleoptera data (subset with family-level identification) linked to vacuum/sweep samples.
- File 10: F3UES_meadow-expt_soils-C-N-pH.csv — soil chemistry data (Total N, Total C, pH) by plot and depth (0–10 cm, 11–20 cm).
- File 11: F3UES_meadow-expt_soils-PLFA.csv — soil microbial community fingerprints via PLFA (fatty acid markers; C, N, and microbial group indicators; PC scores).

- Key data linkages:
  - PlotID and Site tie plant, invertebrate, and soil data together
  - OriginalTttmt, TtmtYear, TtmtDiv, TtmtStruct encode treatment designations
  - Taxonomic and functional classifications across multiple files (e.g., Domin DA FOR scales, OTUs for DNA data, Coleoptera family data)

## Methods and data provenance
- Botanical surveys:
  - 1 m2 quadrats (five per plot) with Domin cover estimates
  - Additional plot-level surveys using DAFOR and flowering extents
- Invertebrates:
  - Summer and autumn sampling by sweep net and vacuum; winter sampling in selected sites
  - Visual surveys around plot edges for observer-focused biodiversity checks
  - Coleoptera identified to family (subset) for finer resolution
- Soil and microbial data:
  - Soil C, N, pH measured by standard elemental analysis
  - Microbial community characterized by PLFA and DNA sequencing (ITS for fungi, 16S for bacteria)
  - DNA sequences deposited in NCBI BioProject PRJNA531648
- Data processing:
  - OTU clustering at 97% identity; taxonomy via QIIME with Greengenes (16S) and UNITE (ITS)
  - PLFA data processed with PCA; Bray-Curtis dissimilarities used for community comparisons

## Accessibility and related resources
- Related primary publication:
  - Norton et al. (2019) Urban Meadows as an alternative to short mown grassland: effects of composition and height on biodiversity (Ecological Applications, in press)
- Supplementary materials:
  - Site maps: F3UES_meadows-expt_site-maps.pdf
- Data availability:
  - DNA data deposited to NCBI BioProject PRJNA531648
  - Supplementary information and related studies available (stakeholder perspectives, public perception)

## Data quality, challenges, and caveats
- Site-specific deviations in treatments and plot availability:
  - Some sites had reduced treatment sets or were terminated early (e.g., Brickhill Heights + Robin Hill; Jubilee Park re-sown; Goldington rotovation)
- Sampling and recording caveats:
  - Variability in mowing schedules; at times plots were mown shortly before sampling
  - DAFOR and Domin scales introduce subjectivity; grass-dominant plots sometimes recorded as 0 cover
  - Taxonomic resolution varies by data type (e.g., many invertebrate groups reported at order level; Coleoptera to family)
- Data gaps:
  - Cranfield site datasets primarily for soils; some summer invertebrate data missing (NA)
  - Actual sampling dates sometimes differed from planned calendar dates

## Implications for data leadership and use
- Rich, multi-taxon, multi-omics dataset enabling cross-taxa analyses of how vegetation height and diversity influence urban biodiversity and soil microbial communities.
- Allows integrated analyses across:
  - Plant community composition and flowering dynamics
  - Aboveground invertebrate communities (sweep/vacuum/visual)
  - Belowground microbial communities (PLFA and DNA-based profiles)
  - Soil chemical properties (C, N, pH) and depth-related variation
- Strong potential for cross-site synthesis and policy-relevant insights on urban meadow design and management.
- Data governance considerations:
  - Ensure robust linkage across 11 CSV files via PlotID/Site and treatment codes
  - Maintain provenance with the original treatment mapping and site metadata
  - Facilitate discoverability and re-use by aligning with the published study and supplementary materials
  - Consider integration with stakeholder and public perception studies for broader impact

## Contact and provenance notes
- Data produced by collaborating institutions: University of Sheffield, Cranfield University, University of Warwick
- Grant support: F3UES project grants NE/J015369/1 and NE/J015067/1
- Primary references and acknowledgments provided in the document, along with methodological derivations from Norton et al. 2019
- DNA sequence data: BioProject PRJNA531648 (NCBI)
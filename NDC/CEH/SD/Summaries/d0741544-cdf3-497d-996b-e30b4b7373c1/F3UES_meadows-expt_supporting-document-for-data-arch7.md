# Supporting document for dataset: Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK

- Purpose and context
  - Provides methodological details, data collection protocols, and interpretation guidance for the dataset on biodiversity responses to vegetation height and diversity in perennial meadow plantings.
  - Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the BESS programme.
  - Focuses on field-scale meadow treatments sown in urban greenspaces in Bedford, Luton, and Cranfield (UK) to quantify effects of floristic diversity and height on plant, invertebrate, soil microbial communities.

- Study sites, timeline, and layout
  - Sites: six greenspaces in Bedford and Luton, plus Cranfield University (urban-adjacent).
  - Establishment: meadows hand-sown in May 2013 on clay-loam soils; plots generally 250 m² (Cranfield plots 50 m²).
  - Treatments: nine meadow treatments created from all combinations of plant height (short, medium, tall) and species richness (low, medium, high).
  - Plot arrangement: standardised rectangles with 5 m gaps to existing mown grass; unmanipulated control area surveyed alongside treatments.
  - Notable site notes: some sites faced space constraints or management changes; Robin Hill discontinued mid-2014; Jubilee Park re-sown in 2014 due to establishment issues.

- Treatments and plot design
  - Height treatments (H1, H2, H3) correspond to:
    - H1: Short, cut roughly every 4–6 weeks to 0.05 m
    - H2: Medium, cut twice per year (April & September)
    - H3: Tall, cut once per year (February); target heights approximately 0.5 m (medium) and 1.5 m (tall)
  - Diversity treatments (D1, D2, D3) correspond to:
    - D1: Low richness (3–4 spp, grasses only)
    - D2: Medium richness (9–13 spp, grass & forb mix)
    - D3: High richness (16–21 spp, grass & forb mix)
  - Seed mixes: perennial, native to southern England; composition varied to achieve target heights and floral cover under mowing regimes; D1 plots were mainly grasses, with some reseeding and density changes over time.
  - Plot sizes: 250 m² at most sites; Cranfield plots 50 m² due to space constraints.

- Data collected (plants, invertebrates, soils, microbes)
  - Botanical data
    - Quadrat surveys (2014–2015): 5 replicate 1 m² quadrats per plot; Domin scale; separated into sown vs non-sown species.
    - Plot-level surveys (observer-focused): DAFOR abundance and flowering cover estimated in four sections per plot; flowering coverage categorized into eight percentage classes.
  - Invertebrates
    - Aboveground sampling: summer and autumn sweeps and vacuum sampling across plots.
    - Winter sampling: February 2016 at select sites to assess overwintering invertebrates.
    - Visual surveys (2014–2015): observer-based counts by taxonomic group (e.g., butterflies, bees, beetles, dragonflies) around plot edges.
    - Biomass: derived from a 2013 broader urban survey; mean dry weight estimates used to convert abundance to biomass for some taxa.
    - Coleoptera detail: adults identified to family for a subset of sites; taxa recorded for taxa-level diversity and composition analyses.
  - Soils and microbial communities
    - Soil sampling: two depths (0–10 cm and 11–20 cm) with three cores per sub-plot per plot; measures include total nitrogen (N), total carbon (C), and pH.
    - Soil microbial phenotype: PLFA analysis to characterize microbial community structure (fungal vs bacterial indicators; PCAs used to summarize community structure).
    - DNA-based analyses: ITS (fungal) and 16S rRNA (bacterial) amplicon sequencing; OTU clustering at 97% identity; taxonomy via Greengenes (16S) or UNITE (ITS); diversity metrics (Fisher's alpha) and Bray-Curtis dissimilarities used to compare plots to unmanipulated controls.
    - DNA data: deposited to NCBI BioProject PRJNA531648.
  - Data structure and variables
    - 11 CSV data files with links across files via common keys (PlotID, Site, Ttmt, Year, etc.).
    - Files include treatment definitions, plant quadrat data, plot-level plant surveys, invertebrate sampling programs, winter invertebrate data, visual invertebrate surveys, vacuum/sweep invertebrate data, Coleoptera data, soil C/N/pH data, and PLFA data.
    - Key linking variables:
      - PlotID: unique per plot, links to treatment and site metadata.
      - OriginalTttmt: historical treatment code linkage.
      - Ttmt.Div and Ttmt.Struct: diversity and height treatment codes.
      - TtmtYr: year since establishment (0, 2, 3; Jubilee Park re-sown affects timeline).
    - Site maps: supplementary document F3UES_meadows-expt_site-maps.pdf provides plot layouts.

- Data structure and files (summary)
  - File 1: F3UES_meadows-expt_treatments-plants.csv — links site, plot, treatment codes (H.D), year, and original designations.
  - File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv — quadrat-level plant composition and sown/non-sown status.
  - File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv — plot-level plant observations (DAFOR and flowering).
  - File 4: F3UES_meadows-expt_inverts_sampling-programme.csv — sampling program identifiers to link invertebrate data files.
  - File 5: F3UES_meadows-expt_inverts_winter.csv — winter invertebrate data.
  - File 6: F3UES_meadows-expt_inverts_visual-surveys.csv — observer-based visual invertebrate surveys.
  - File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv — vacuum and sweep invertebrate data.
  - File 8: F3UES_meadows-expt_inverts_biomass.csv — biomass estimates for invertebrates.
  - File 9: F3UES_meadows-expt_inverts_Coleoptera.csv — Coleoptera data (family-level counts).
  - File 10: F3UES_meadow-expt_soils-C-N-pH.csv — soil C, N, and pH data by plot and depth.
  - File 11: F3UES_meadow-expt_soils-PLFA.csv — PLFA-derived microbial community characteristics.
  - Notes: DNA sequencing data deposited (PRJNA531648); supplementary methods and site maps provided; related publications document management and public engagement aspects.

- GIS and mapping considerations
  - Spatial scope: urban meadows in Bedford and Luton, with at-scale site coordinates in data files; Cranfield site included as adjacent rural-urban interface.
  - Map-ready attributes: site, plot IDs, treatment codes (height and diversity), year since establishment, and multiple ecological response variables (plants, invertebrates, soils, and microbial indicators).
  - Potential geospatial products:
    - Plot-level biodiversity indices by height/diversity treatment.
    - Temporal maps showing changes across years (0, 2, 3 years after planting) for plant cover, invertebrate activity, soil properties, and microbial indicators.
    - Spatial comparisons between sites and between manipulated plots vs unmanipulated controls.
  - Additional resources: supplementary site-maps PDF to aid plot-level visualization and layout in GIS.

- Related resources and references
  - Core publication: Norton et al. (2019) Urban meadows as an alternative to short mown grassland: effects of composition and height on biodiversity (Ecological Applications, in press).
  - Methodological basis for data descriptions and interpretation drawn from Norton et al. 2019.
  - Supplementary data: F3UES_meadows-expt_site-maps.pdf for plot layouts.
  - Additional related studies on meadow management, public perception, and urban biodiversity context referenced in the document.

- Access and data provenance
  - Raw DNA soil sequencing data deposited in NCBI BioProject PRJNA531648.
  - Data available as 11 CSV files with explicit linking keys to enable integration and GIS-ready analysis.
  - Documentation provides clear guidance on data interpretation, variable definitions, and units to support reliable mapping and spatial analyses.
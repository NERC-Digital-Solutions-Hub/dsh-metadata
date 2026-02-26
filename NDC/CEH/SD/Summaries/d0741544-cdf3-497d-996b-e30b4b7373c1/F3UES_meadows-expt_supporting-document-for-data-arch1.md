# Supporting document for dataset: Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK.

- Purpose of the dataset
  - Quantify how floristic diversity and vegetation height influence biodiversity across plants, invertebrates, and soil microbial communities.
  - Use a replicated, field-scale manipulation to assess relative roles of species richness and height on ecosystems in urban greenspaces.

- Experimental design and meadow establishment
  - Location: six sites across Bedford and Luton in Southern England, plus Cranfield University.
  - Meadows sown in May 2013 (with re-sowing and weeding as needed) on clay-loam soils; one site (Jubilee Park) re-sown in 2014.
  - Plots: 250 m2 (50 m2 at Cranfield); arranged in a grid with at least 5 m gaps from mown grass.
  - Unmanipulated control plots consisted of adjacent short-mown grass areas.

- Treatments (height and diversity)
  - Nine meadow treatments from all combinations of height (short, medium, tall) and diversity (low, medium, high).
  - Height parameters reflect mowing regimes and target vegetation heights:
    - Short: cut every 4–6 weeks (target ~0.05 m)
    - Medium: cut twice per year (April & Sept; ~0.50 m during growing season)
    - Tall: cut once per year (February; ~1.50 m typical maximum)
  - Diversity parameters:
    - Low (grass-only) - D1
    - Medium (grass & forbs) - D2
    - High (grass & forb mix) - D3
  - Seed mixes varied across treatments to achieve target heights and floral cover; total species richness per treatment ranged from 3–21 species depending on height/diversity.

- Plant, invertebrate, and soil data collection
  - Botanical surveys (2014–2015): two scales
    - Quadrat surveys (five 1 m2 quadrats per plot; Domin scale; sown vs. non-sown species)
    - Plot-level surveys (edge visibility; DAFOR-based abundance; flowering percentage)
  - Invertebrates
    - Aboveground sampling in summer and autumn (two sessions per year; multi-method approach: sweep nets, vacuum, hand searches)
    - Winter sampling in 2016 to assess overwintering potential (subset of sites)
    - Additional visual surveys (articulated observer-based counts) in select years
    - Biomass estimates derived from subsampled invertebrates; collection included orders and family-level identifications where feasible
  - Soils
    - Sampling at three plots per site (two depths: 0–10 cm and 11–20 cm)
    - Measures: total nitrogen, total carbon, pH
    - Microbial community assessments via PLFA (bacterial vs fungal indicators; PCAs)
    - DNA-based analyses: ITS (fungi) and 16S rRNA (bacteria) amplicon sequencing; OTUs at 97% identity; taxonomic assignment to GEO databases; alpha diversity (Fisher’s alpha) and Bray-Curtis dissimilarities relative to controls
  - DNA sequencing data deposited to NCBI BioProject PRJNA531648

- Data structure and files (11 CSV files)
  - File 1: F3UES_meadows-expt_treatments-plants.csv
    - Links plots to site, PlotNo, treatment codes (D1–D3, H1–H3), year, and years since planting
  - File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv
    - Quadrat-level plant species data; year/treatment/site/PlotID; species; sown status; Domin cover to percent
  - File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv
    - Plot-level plant surveys; species visibility, flowering cover; DAFOR-derived values; recorder notes
  - File 4: F3UES_meadows-expt_inverts_sampling-programme.csv
    - Sampling program metadata linking samples to plots, methods (Vac, Sweep, Hand Search, visual laps), dates, seasons
  - File 5: F3UES_meadows-expt_inverts_winter.csv
    - Winter invertebrate survey data (taxonomic notes; life stage; abundances)
  - File 6: F3UES_meadows-expt_inverts_visual-surveys.csv
    - Visual invertebrate surveys (observed taxa by observer; order and lower taxonomic units; notes on limited identifications)
  - File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv
    - Vacuum and sweep invertebrate samples; taxonomic classifications; abundances
  - File 8: F3UES_meadows-expt_inverts_biomass.csv
    - Dry weight biomass data for invertebrate taxa; per-taxon mean weights and counts
  - File 9: F3UES_meadows-expt_inverts_vac-and-sweep-samples_Coleoptera.csv
    - Coleoptera data from Vac/Sweep samples; counts by family
  - File 10: F3UES_meadow-expt_soils-C-N-pH.csv
    - Soil chemistry data: site, plot, depth, nitrogen, carbon, pH, replication
  - File 11: F3UES_meadow-expt_soils-PLFA.csv
    - Soil PLFA profiles: fatty acid abundances (various markers for fungi and bacteria), PC1–PC3 coordinates

- Data processing and analysis notes
  - DNA data (OTU table and taxonomic assignments) are available; fungal vs bacterial components analyzed separately
  - Alpha diversity (Fisher’s alpha) calculated for microbial communities; Bray-Curtis dissimilarities used to compare plots to unmanipulated controls
  - PLFA data summarized as relative abundances; PCAs performed to summarize microbial community structure
  - Plant data distinguish sown vs non-sown species; Domin scale converted to percent cover for per-plot averages
  - Invertebrate data include multiple taxonomic resolutions (order-level to family-level for Coleoptera; some groupings for Diptera, Hymenoptera, Lepidoptera)

- Site and study context
  - Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project; tied to the Biodiversity and Ecosystem Service Sustainability (BESS) program
  - Rationale and detailed methods presented in Norton et al. (2019); additional site maps and stakeholder studies referenced
  - Related datasets and supplementary documents available (site maps; background literature; public outreach/work)

- Practical considerations for analysts
  - Data are organized to link plot-level treatments to site, year, and sampling method
  - Some plots (e.g., at Brickhill Heights and Robin Hill) experienced treatment changes or discontinuations during the study; such notes are documented in the metadata
  - Several datasets require careful handling of zero or missing values (e.g., Domin scale categories converted to percent; NR notations in flowering data)
  - DNA sequence data accessible via GenBank/NCBI BioProject PRJNA531648 for reproduction and meta-analyses
  - Core analyses can test hypotheses about how increasing height or diversity influences plant diversity, invertebrate diversity/biomass, and soil microbial community structure

- Key references and additional information
  - Norton et al. 2019: Urban meadows as an alternative to short mown grassland; Ecological Applications (main results and methods)
  - Supplemental materials: Appendix S1 figures/tables; site maps; qualitative stakeholder studies
  - Sequencing and bioinformatics references provided (QIIME, UPARSE, Trimmomatic, Greengenes/UNITE, etc.)

- Access and reuse
  - Data are provided as 11 CSV files with detailed variable definitions
  - DNA data deposited in NCBI BioProject PRJNA531648
  - Related publications and supplementary documents cited for background and interpretation
# Supporting document for dataset: Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK

- Provides detailed experimental design, data collection methods, and interpretation aids for a field-scale manipulation study of urban meadow biodiversity.
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the BESS programme; aims to quantify how plant diversity and structure (height) influence biodiversity across plants, invertebrates, and soil microbial communities.
- Multi-institution collaboration (University of Sheffield, Cranfield University, University of Warwick) with the University of Sheffield leading the field experiments.

## Study scope and aims

- Location: six urban greenspaces in Bedford and Luton, UK; plus Cranfield University site.
- Experimental design: replicated set of nine meadow treatments combining three height levels (short, medium, tall) and three plant diversity levels (low, medium, high).
- Objective: determine the relative roles of floristic diversity and vegetation height on biodiversity and community composition across plants, invertebrates, and soil microbes; also assess potential implications for urban meadow management and policy guidance.

## Experimental design and meadow establishment

- Plot design: plots are 250 m2 (12.5 m × 20 m) at most sites; Cranfield plots are smaller at 50 m2 (5 m × 10 m) due to space.
- Treatments: nine combinations of height and diversity (H1/H2/H3 for short/medium/tall; D1/D2/D3 for low/medium/high diversity). An unmanipulated control area is surveyed for comparison.
- Seed mixes: all sown species are perennials native to southern England; seed mixes varied to meet target height and floral cover per treatment.
- Establishment and maintenance: initial weed control and reseeding as needed; some site-specific adjustments due to space and resident feedback (e.g., Goldington Green, Brickhill Heights, and Robin Hill adjustments).
- Site overview: plots placed in areas adjacent to housing or campus settings on clay-loam soils; general management continued for the surrounding mown grassland in the unmanipulated control.

## Data collected and taxonomic scope

- Plants
  - Botanical surveys in 2014–2015 using 1 m2 quadrats (five per plot) to record species cover (Domin scale) and separate sown vs non-sown species.
  - Plot-level flowering and visibility surveys (DAFOR-like) conducted in 2014–2015 to capture observer-perceived species richness and flowering cover.
- Invertebrates
  - Aboveground invertebrates sampled in summer and autumn across plots (and winter surveys in 2016 for overwintering communities at select sites).
  - Methods include sweep netting, vacuum sampling, and hand searches; visual surveys conducted to capture observer-perceived diversity by taxa.
  - Coleoptera identified to family for enhanced resolution in three sites with full treatment sets.
  - Biomass estimates derived from a subset of samples; standardization to compare across plots and sites.
- Soils and microbial communities
  - Soil cores (0–10 cm and 11–20 cm) collected February 2015 from multiple plots; analyzed for total carbon, total nitrogen, and pH.
  - Microbial community characterized by PLFA (phospholipid fatty acids) analysis and microbial biomass C via fumigation-extraction; DNA-based profiling (16S rRNA for bacteria and ITS for fungi) from soil DNA, with OTU clustering at 97% identity.
  - DNA sequencing data deposited in NCBI BioProject PRJNA531648.
- Data outputs and structure
  - 11 CSV data files cover treatments, plants, quadrat surveys, plot-level surveys, invertebrate sampling (vacuum and sweep), visual surveys, winter invertebrates, invertebrate biomass, Coleoptera data, soils C-N-pH, and PLFA data.
  - Data linked by PlotID and treatment codes; Year (H.D.Y) and OriginalTttmt fields connect samples to their experimental context.

## Data structure and key variables

- File 1: F3UES_meadows-expt_treatments-plants.csv
  - Linkage of plots to site, treatment (D diversity, H height), year since sowing, and original treatment codes.
- File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv
  - Species per plot per quadrat; whether species were sown; Domin cover estimates; percent cover derived from Domin classes.
- File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv
  - Plot-level observations of conspicuous species, flowering cover, and observer notes (DAFOR-based).
- File 4: F3UES_meadows-expt_inverts_sampling-programme.csv
  - Sampling schedule, methods, and linkage to plots/sites for invertebrate data.
- File 5: F3UES_meadows-expt_inverts_winter.csv
  - Winter invertebrate survey data; taxonomic depth and abundance.
- File 6: F3UES_meadows-expt_inverts_visual-surveys.csv
  - Visual invertebrate surveys by observer, taxon category guidance, and Abund counts.
- File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv
  - Vacuum and sweep invertebrate samples; taxonomic classifications and abundances.
- File 8: F3UES_meadows-expt_inverts_biomass.csv
  - Dry weight biomass data by taxon, used to infer biomass from abundances.
- File 9: F3UES_meadows-expt_inverts_vac-and-sweep-samples_Coleoptera.csv
  - Coleoptera data from the same samples, identified to family.
- File 10: F3UES_meadow-expt_soils-C-N-pH.csv
  - Soil total nitrogen, total carbon, and pH by plot and depth.
- File 11: F3UES_meadow-expt_soils-PLFA.csv
  - PLFA-based microbial community composition by taxa; diversity and principal component scores.

## Data availability and governance

- DNA-based microbial data deposited in NCBI BioProject PRJNA531648.
- Site maps and supplementary materials referenced (F3UES_meadows-expt_site-maps.pdf).
- Key analyses and interpretation discussed in Norton et al. (2019) Ecological Applications (methods description substantially drawn from this paper).
- Data sharing aims to support monitoring frameworks, with explicit linking of data to site, plot, year, and treatment enabling policy-relevant analyses.

## Practical considerations for monitoring frameworks

- Indicators and metrics demonstrated
  - Plant diversity and structure: species richness by treatment, functional group composition (grass vs forbs), and floral resources.
  - Invertebrate diversity and abundance: multi-taxa surveys (sweep, vacuum, hand-search, visual) with both order-level and family-level resolution (Coleoptera), enabling richness, evenness, and community composition analyses.
  - Soil biology and chemistry: carbon and nitrogen pools, pH, microbial biomass, PLFA-based community structure, and DNA-based microbial diversity.
- Study design strengths for monitoring
  - Fully factorial design across height and diversity with replication, enabling evaluation of policy-relevant vegetation management regimes.
  - Multi-taxa, multi-domain data collection (plants, invertebrates, soil microbes) in urban greenspaces, supporting comprehensive ecological monitoring.
  - Standardized protocols and detailed metadata linking plots, treatments, and sampling events, facilitating comparability and reproducibility.
- Data governance and usability
  - Public sharing of datasets with clear provenance and metadata supports transparency and policy evaluation.
  - Data are structured to support indicator development, cross-site comparisons, and temporal trend analyses.
- Limitations and considerations
  - Some site-specific deviations and plot-level constraints (e.g., site size, resident feedback, management changes) may affect generalizability; documentation of these deviations aids interpretation.
  - Longitudinal consistency depends on standardized sampling windows; calendar-year sampling differences and observer variability are noted (DAFOR-based perceptions, visual surveys).
  - Data gaps due to missing plots or treatments at certain sites (e.g., Robin Hill discontinued; some sites had partial treatment sets) should be accounted for in analyses.

## End notes and related resources

- Core publication for methods and outcomes: Norton et al. 2019, Urban meadows as an alternative to short mown grassland: effects of composition and height on biodiversity (Ecological Applications; in press at the time of this document).
- Supplementary materials and site maps referenced for deeper interpretation.
- Related stakeholder and perception studies provide policy-relevant context for urban meadow management and public acceptance.
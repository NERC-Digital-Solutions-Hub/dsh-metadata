Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK.

## Purpose and scope
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the BESS programme.
- Aims to quantify how floristic diversity and vegetation height affect biodiversity across plant, invertebrate, and soil microbial communities in replicated meadow plantings.
- Data accompany field-scale experiments carried out in six urban greenspaces (Bedford and Luton) with a replicated nine-treatment design.

## Study design and sites
- Establishment: Meadows established in 2013 on clay-loam soils adjacent to residential areas; six sites in Bedford and Luton, plus Cranfield University (countryside-adjacent urban features).
- Plots: 250 m2 plots (12.5 m × 20 m) at most sites; Cranfield plots are smaller (50 m2) due to space constraints.
- Treatments: Nine meadow treatments from the cross of plant height (short H1, medium H2, tall H3) and plant diversity (low D1, medium D2, high D3). Seed mixes composed of perennial natives; plots separated by at least 5 m from adjacent mown grass.
- Unmanipulated control: An area of original short mown grass within each site was surveyed as an unmanipulated control.
- Site modifications: Some sites experienced adjustments (e.g., Goldington Green space constraints; Brickhill Heights/Robin Hill discontinuation; Jubilee Park re-sown; one site reestablishment in 2014).  

## Treatments and seed composition
- Height treatments: Short (H1) cut every 4–6 weeks; Medium (H2) cut twice annually; Tall (H3) cut once annually.
- Diversity treatments: Low (D1, grasses only); Medium (D2, grass+forbs mix); High (D3, enriched grass+forbs mix).
- Seed mixes: Vary by treatment to achieve target heights and floral cover under mowing regimes; exact species composition provided in accompanying tables (seed density and species abbreviations noted in the dataset documentation).

## Data collection methods and timing
- Botanical surveys (plants)
  - timing: 2014 and 2015; years since establishment noted (year 0 to year 3 for some sites).
  - method: five replicate 1 m2 quadrats per plot, Domin scale for percent cover; separate sowed vs non-sowed species.
  - additional plot-level surveys: DAFOR-based visual assessments of abundance and estimates of flowering cover in 2014–2015.
- Invertebrates
  - aboveground surveys: summer and autumn sampling in year 2 post-sowing; some sites extended into year 3; visual observational surveys in 2014–2015.
  - winter sampling: February 2016 at several sites to assess overwintering invertebrates.
  - methods: sweep net and vacuum sampling; hand-searching in winter; transects and sampling containers to prevent escape; Coleoptera identified to family level (for deeper analysis); additional visual surveys by an experienced entomologist.
  - biomass: derived from subsamples across sites; oven-dried to determine biomass per taxon.
- Soil and microbial assessments
  - soil sampling: conducted at Chiltern Avenue, Bramingham Road, and Cranfield in 2015; three subplots per plot; bulk samples at 0–10 cm and 11–20 cm.
  - soil chemistry: total nitrogen and carbon, pH measured.
  - microbial communities: PLFA analysis for microbial community structure and biomass; DNA extraction for fungi (ITS) and bacteria (16S); sequencing via Illumina MiSeq; OTU clustering at 97% identity; taxonomy via QIIME (Greengenes for 16S, UNITE for ITS).
  - data products: microbial community composition summarized by PCAs and OTU-level diversity; Bray-Curtis dissimilarities used to compare plots to unmanipulated controls.
- Data management and deposition
  - sequencing data: deposited in NCBI BioProject PRJNA531648.
  - data files: 11 CSV files detailing treatments, quadrat data, plot surveys, invertebrate sampling, winter invertebrates, visual invertebrate surveys, VAC/Sweep sampling, biomass, Coleoptera, soils (CNpH), and soils PLFA.

## Data structure and files
- File 1: F3UES_meadows-expt_treatments-plants.csv — links plots to site, plot ID, original treatments, and calendar year.
- File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv — quadrat-level plant data (domin cover) by year and plot.
- File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv — plot-level observer surveys (DAFOR and flowering estimates).
- File 4: F3UES_meadows-expt_inverts_sampling-programme.csv — description of sampling events and methods per plot/season.
- File 5: F3UES_meadows-expt_inverts_winter.csv — winter invertebrate data.
- File 6: F3UES_meadows-expt_inverts_visual-surveys.csv — observer-based invertebrate visual surveys.
- File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv — vacuum and sweep invertebrate samples.
- File 8: F3UES_meadows-expt_inverts_biomass.csv — biomass estimates for invertebrates.
- File 9: F3UES_meadows-expt_inverts_vac-and-sweep-samples_Coleoptera.csv — Coleoptera data (family-level) from VAC/Sweep samples.
- File 10: F3UES_meadow-expt_soils-C-N-pH.csv — soil C, N, and pH data by plot, depth, and replication.
- File 11: F3UES_meadows-expt_soils-PLFA.csv — PLFA-derived microbial community data (fungal/bacterial indicators, PC axes).

## Data processing, analyses, and related work
- Data analysis and presentation are aligned with Norton et al. (2019) Ecological Applications (urban meadows as an alternative to short mown grassland), with methods detailed in this document forming the data collection and processing backbone.
- Supplementary materials include site maps and additional background on management and stakeholder perspectives.
- DNA data and microbial analyses are integrated and deposited publicly for cross-study use.

## Accessibility and related resources
- Primary data sources: 11 CSV data files described above.
- DNA sequencing data: accessible via NCBI BioProject PRJNA531648.
- Related publications and supplementary materials provide background, maps, and stakeholder context (Norton et al. 2019; Hoyle et al. 2017; Southon et al. 2017, 2018).

## Use for environmental monitoring and analysis
- Provides standardized, multi-taxa biodiversity data linked to explicit habitat manipulations (height and diversity) in urban green spaces.
- Enables time-series and cross-site comparisons, supporting assessment of policy relevance for urban meadow designs.
- Dataset structure supports integration with other urban biodiversity datasets, with explicit cross-links between plots, treatments, years, and sampling methods.
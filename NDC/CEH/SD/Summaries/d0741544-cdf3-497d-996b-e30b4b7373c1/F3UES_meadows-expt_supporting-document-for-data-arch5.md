# Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK.

## Aim and context
- Report details the design, data collection methods, and supporting information for a dataset generated under the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, within the BESS programme.
- Objective: quantify how floristic diversity and vegetation height in perennial urban meadow plantings affect biodiversity and ecosystem components (plants, invertebrates, soil microbes) in two UK towns (Bedford and Luton) with additional Cranfield University plots.
- Experimental design: nine meadow treatments created from all combinations of three height levels (short, medium, tall) and three plant species richness levels (low, medium, high), sown in plots across six sites (plus Cranfield University), including an unmanipulated control. Plot sizes varied by site (typically 12.5 m x 20 m; Cranfield plots 5 m x 10 m).
- Timeframe: plots established in 2013 (some re-establishment and adjustments through 2014); surveys conducted in 2014–2015 (plants and invertebrates), with winter invertebrate sampling in 2016.

## Organizations and data governance
- Lead institutions: University of Sheffield (lead management and data collection), Cranfield University (soils analyses), University of Warwick (soil microbial analyses).
- Data and analyses underpin a published Ecological Applications study (Norton et al., 2019) and related stakeholder and perception research.
- Supporting materials include site maps and supplementary documents; DNA sequencing data are deposited in public repositories (see Data Accessibility).

## Data collection overview and types
- Botanical data:
  - Quadrats: 1 m² quadrats per plot to estimate species cover (Domin scale); splits into sown vs non-sown species.
  - Plot-level surveys: observer-based assessments of visibly noticeable species and flowering cover (DAFOR-based, eight flowering categories converted to percentages).
- Invertebrates:
  - Aboveground sampling: sweep Net and vacuum methods in summer and autumn; winter sampling in select sites (2016) to assess overwintering fauna.
  - Visual surveys: observer-based counts by an entomologist in multiple years to capture species seen by a passerby.
  - Biomass: subset of specimens used to estimate dry weight per taxon; subsequent conversions to biomass for comparisons.
  - Coleoptera: subset of samples identified to family to refine diversity assessments.
- Soil characteristics:
  - Chemistry: total nitrogen and total carbon at two depths (0–10 cm, 11–20 cm).
  - pH measurements.
  - Microbial community: PLFA profiling (fatty acid indicators for fungi and bacteria) and microbial biomass C via fumigation-extraction.
  - DNA-based microbial surveys: ITS (fungal) and 16S rRNA (bacterial) amplicon sequencing; OTU clustering at 97% identity; taxonomic assignment via QIIME using Greengenes and UNITE databases; diversity metrics and Bray-Curtis dissimilarities used to compare treatments to unmanipulated controls.
- Data provenance and linkage:
  - Data are organized across 11 CSV files, all linked via a PlotID and treatment codes (H for height, D for diversity) with Year/TtmtYear indicating years since sowing.
  - DNA sequencing data deposited publicly (BioProject PRJNA531648).

## Data structure and key files
- File 1: F3UES_meadows-expt_treatments-plants.csv — links site, plots, original treatment codes, year, diversity/height designations, and plotting year.
- File 2: F3UES_meadows-expt_plant-quadrat-surveys.csv — quadrat-level plant data (year, site, plot, species, sown status, percent cover).
- File 3: F3UES_meadows-expt_plant-plot-level-surveys.csv — plot-level, observer-based plant and flowering cover data (DAFOR-based, flowering percentages).
- File 4: F3UES_meadows-expt_inverts_sampling-programme.csv — sampling program metadata linking to samples across plots/sites/methods.
- File 5: F3UES_meadows-expt_inverts_winter.csv — winter invertebrate survey data (taxonomic levels and abundances).
- File 6: F3UES_meadows-expt_inverts_visual-surveys.csv — visual invertebrate survey data (taxa seen, abundances, and classification).
- File 7: F3UES_meadows-expt_inverts_vac-and-sweep-samples.csv — vacuum and sweep invertebrate data (taxonomic levels and abundances).
- File 8: F3UES_meadows-expt_inverts_biomass.csv — dry weight biomass values by taxon for sampled invertebrates.
- File 9: F3UES_meadows-expt_inverts_vac-and-sweep-samples_Coleoptera.csv — Coleoptera data from vacuum/sweep samples, identified to family.
- File 10: F3UES_meadow-expt_soils-C-N-pH.csv — soil chemistry and pH per plot/depth with replication info.
- File 11: F3UES_meadows-expt_soils-PLFA.csv — PLFA-based microbial community profiles (fungal/bacterial indicators, PC1–PC3, and other fatty-acid indicators).

## Provenance, quality, and limitations
- Experimental notes highlight site-specific adaptations and disruptions:
  - Some sites had limited or altered treatment sets due to space, resident feedback, or management actions (e.g., Goldington Green, Brickhill Heights, Jubilee Park).
  - Re-seeding and weed management were undertaken to aid meadow establishment; some plots required re-sowing or abandonment of certain treatments.
  - Cranfield plots were smaller and used primarily for soil analyses.
- Data collection reflects two primary years post-establishment for plant and invertebrate surveys, with a later winter sampling in 2016 to assess overwintering fauna.
- Data processing steps include standardized methods for sequencing, OTU clustering, and PLFA analysis; taxa data include notes on dead/alive status and identification limitations; some data are reported at broader taxonomic levels to reflect method constraints.

## Data accessibility and related materials
- Primary dataset described here is intended for reuse in conjunction with Norton et al. (2019) and related publications.
- DNA sequencing data are publicly accessible via NCBI BioProject PRJNA531648.
- Maps and supplementary materials (e.g., site maps) are provided in accompanying documents (e.g., F3UES_meadows-expt_site-maps.pdf).
- Related research covers management, public perception, and aesthetic-value aspects of urban meadow plantings.

## Practical considerations for data stewards and reuse
- The dataset provides rich multilevel data (plots, treatments, years, multiple taxa and communities) suitable for cross-domain analyses of biodiversity responses to management.
- Key integration points across files rely on PlotID, Year/TtmtYear, site codes, and H.D treatment codes; careful attention to these linkages is essential for cross-file analyses.
- Documentation notes, seed mix details, and treatment definitions (H1–H3, D1–D3) support reproducibility and replication in meta-analyses.
- For genomic and microbial analyses, ensure proper interpretation of OTU-based diversity metrics and PLFA indicators, with awareness of potential taxonomic resolution limits and context-specific interpretation.

## Summary of relevance for data governance
- Comprehensive metadata structure, clear treatment/place identifiers, and explicit linking mechanisms support discoverability and reuse across researchers and institutions.
- Public deposition of DNA sequence data and clear provenance statements enhance data integrity and long-term accessibility.
- Documentation of site-specific deviations and data collection nuances supports transparency about data quality and applicability to different contexts.
# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

- A dataset documenting the relative abundances of antimicrobial resistance (AMR) genes detected in soil DNA from soils around Newcastle upon Tyne, NE England.
- Field design preselected locations based on metal concentrations and land-use, representing four treatments: low-metal/rural, low-metal/urban, high-metal/rural, and high-metal/urban.
- Sampling conducted in June 2016 from the upper soil horizon (0–15 cm) and samples were refrigerated for processing.

## Field sampling and study design

- Preselection of sampling sites informed by previous work on metal concentrations (Rothwell and Cooke, 2015) and land-use patterns.
- Four treatment combinations to explore metal effects and urban vs rural contexts.

## Analytical methods

- DNA extraction: Community DNA extracted from soils using the FastDNA Spin Kit for Soil; samples stored at -80°C.
- DNA processing: 500–2000 ng DNA was freeze-dried and sent for high-throughput AMR gene analysis to the Institute of Urban Environment, Chinese Academy of Sciences (Xiamen, China).
- Quantification: Quantitative PCR performed with Applied Biosystems OpenArray platform, using primers and methods established in prior work (e.g., Zhu et al. 2013, 2017; Looft et al. 2012).
- Detection limit: Threshold cycle (Ct) of 37 used as the detection cutoff.

## Data units and normalization

- AMR gene units: Relative gene abundances, calculated using the delta-delta Ct (2^-ΔΔCt) method.
- Normalization surrogate: 16S rRNA levels measured to estimate total bacterial abundance.

## Data structure and content

- Main data rows are organized around Table 1, mapping ARDB (Antibiotic Resistance Genes Database) nomenclature to ARDB entries and antibiotic classifications.
- The dataset includes a comprehensive listing of AMR genes across multiple antibiotic classes (e.g., aminoglycosides, beta-lactamases, macrolide-lincosamide-streptogramin [MLSB], sulfonamides, tetracyclines, etc.).
- Entries provide gene symbol, ARDB reference, and antibiotic classification, illustrating broad coverage of resistance determinants.
- 16S rRNA and AMR gene abundances are recorded for each sample, enabling normalization and comparative analyses.

## Data quality, interpretation, and metadata

- Data were generated using a standardized high-throughput qPCR approach with a defined detection limit (Ct ≤ 37).
- Preselection based on metal concentrations and land-use improves the relevance for studying environmental drivers of AMR gene abundance, though it may limit generalizability beyond NE England soils.
- Metadata and data provenance are tracked, with the intention of making datasets discoverable and usable via portals with appropriate metadata (consistent with the analysts' approach to data sharing).

## Potential analyses and uses for analysts

- Assess correlations between AMR gene relative abundances and environmental factors (metal concentration, urban vs rural context, soil depth).
- Compare four treatment groups to identify how metal load and land-use context influence AMR gene profiles.
- Use 16S rRNA normalization to evaluate changes in AMR gene abundance relative to total bacterial load.
- Develop predictive models to estimate AMR gene abundance from environmental variables and site characteristics.
- Integrate this dataset with other environmental microbiome datasets to examine broader patterns of AMR gene distribution and drivers.

## References

- Livak KJ, Schmittgen TD (2001) Analysis of relative gene expression data using realtime quantitative PCR and the 2(-ΔΔCt) method.
- Liu B, Pop M (2009) ARDB - Antibiotic Resistance Genes Database.
- Looft T, et al. (2012) In-feed antibiotic effects on the swine intestinal microbiome.
- Rothwell KA, Cooke MP (2015) Methods for calculating background concentrations of potentially toxic elements in urban soil.
- Zhu Y-G, et al. (2013, 2017) ARDB and environmental AMR gene diversity studies.
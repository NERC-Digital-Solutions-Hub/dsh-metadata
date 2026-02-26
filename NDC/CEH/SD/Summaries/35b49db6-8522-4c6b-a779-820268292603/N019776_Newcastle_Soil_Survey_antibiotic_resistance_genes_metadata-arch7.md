# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

- Study aim: Collation of relative abundances of antimicrobial resistance (AMR) genes detected in DNA extracted from soils around Newcastle upon Tyne, linked to site metal concentrations and land-use; four treatment categories: low-metal/rural, low-metal/urban, high-metal/rural, high-metal/urban.
- Spatial scope: Soil samples collected from locations in the NE England/N Newcastle area; emphasis on spatial variation across urban/rural and metal-exposure contexts.

## Fieldwork

- Sampling period: June 2016.
- Sample depth: Upper horizon, less than 15 cm from surface.
- Sample collection: Preselected locations based on prior metal concentration data and land-use patterns (as per Rothwell and Cooke 2015).
- Handling: Samples refrigerated until processing.

## Analytical methods

- DNA processing: Community DNA extracted from soils using FastDNA Spin Kit for Soil kits; DNA stored at -80°C.
- High-throughput analysis: 500–2000 ng of DNA (per sample) freeze-dried and sent for analyses; performed using Quantitative PCR on the OpenArray platform.
- Primers/methods: Primers and analytical approaches built on previously published methods (e.g., Zhu et al. 2013, 2017; Looft et al. 2012).
- Detection limit: Threshold cycle of 37 used as the detection limit.

## Nature of recorded units

- AMR gene reporting: Relative gene abundances (normalized measures of gene abundance).
- Bacterial load proxy: 16S rRNA levels quantified to provide a surrogate for total bacterial abundance.

## Details of data structure

- Core data representation: Main rows reflect high-throughput qPCR assays with gene nomenclature aligned to the Antibiotic Resistance Database (ARDB).
- Examples of data columns: 16S rRNA, ARDB gene; ARDB gene, antibiotic classification; multiple ARDB gene entries (e.g., aac family, bla family, tet family, erm/mec families, van genes, etc.) with corresponding antibiotic classifications (e.g., Aminoglycoside, Beta-Lactamase, MLSB, Vancomycin resistance, Tetracycline resistance, etc.).
- Table 1 mappings: Extensive gene-to-class mappings and coding used to standardize gene names and associated resistance classifications (including frequent aliases and classifications).
- Data scale: Large, multi-gene matrix linking each sample to numerous AMR gene targets and their classifications.

## Spatial relevance and GIS potential

- GIS-ready attributes: Sample points tied to location context (urban vs. rural, metal exposure categories) and AMR gene abundance proxies.
- Potential analyses: Map spatial distribution of AMR gene relative abundances, assess correlations with metal concentrations and land-use, identify hotspots, and compare across the four treatment categories.

## Data quality and processing considerations

- Field and lab protocols emphasize controlled sample handling (refrigeration, standardized DNA extraction, OpenArray qPCR).
- Relative abundances derived via delta-delta Ct approach; 16S rRNA levels used for normalization to estimate total bacterial load.
- References provided for methods and data interpretation, ensuring traceability and reproducibility.

## References

- Livak, KJ, Schmittgen TD (2001). Analysis of relative gene expression data using real-time quantitative PCR.
- Liu, B., Pop, M. (2009). ARDB - Antibiotic Resistance Genes Database.
- Looft, T. et al. (2012). In-feed antibiotic effects on the swine intestinal microbiome.
- Rothwell, KA., Cooke, MP (2015). Methods for calculating background concentrations of potentially toxic elements in urban soil.
- Zhu, Y-G. et al. (2013, 2017). AMR gene diversity in China and continental-scale pollution in estuaries.
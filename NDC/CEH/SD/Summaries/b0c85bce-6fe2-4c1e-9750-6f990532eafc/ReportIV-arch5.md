# SUMMARY

## Overview
- Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders) focusing on links between soil biodiversity and above-ground plant communities.
- Longitudinal monitoring of above-ground productivity, species composition, and diversity under five main site treatments: Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, plus Insecticide.
- Site management includes regular mowing, fertilisation, liming, insecticide application, and a recent trampling context in C2 plots. Data collected across multiple coordinated projects, with extensive appendices documenting methods and results.

## Data assets and collection

- Datasets and data streams
  - Weather data from on-site Automatic Weather Station (1999–present); headline measures summarized in Appendix 5.
  - Above-ground biomass per plot, measured May–Sept each year (1999–2002); results show a consistent hierarchy by treatment and a general yearly decline in 2002 for many treatments (Appendix 6; Figure 2).
  - Point Analysis surveys (baseline in 1998; annual surveys in 2000–2002) using 0.5 m2 cells and a 100-point grid; bryophyte identification improved in 2002; PCSAs used to separate improved vs unimproved plots (Appendix 3, 8; Figure 5).
  - Soil data: soil pH (5 cm depth) monitored since 1998 with a pronounced lime effect raising pH toward ~7 in 2002; soil moisture measured in 2002 using a theta probe (Appendix 5; Figures 3a–4b).
  - Biomass and species data: annualised biomass per plot (Appendix 6), rank of biomass samples (Appendix 7), and percentage ranks of species by treatment (Appendix 8).
  - Species lists: full vascular plant and bryophyte inventories (Appendix 3).
  - Experimental metadata: detailed site layout with blocks, plots, sub-plots, and 0.5 m × 0.5 m cells; treatment allocations and dates (Appendix 1, Appendix 2).
  - 13CO2 pulse experiments and trace-gas measurements conducted with CEH mobile laboratories in 2002 (text reference to Phase II fieldwork).
- Data collection and measurement protocols
  - Vegetation management: monthly mowing to ~6 cm (May–September); insecticide applied after mowing on insecticide plots; nitrogen and/or lime applied in spring.
  - Sampling design: 5 replicate blocks; 6 main plots per block; treatments allocated randomly; sub-plots and cells designated for different groups (0.5 m2 sampling cells; 25-point baseline quadrat in 1998; 100-point point analysis in 2000–2002).
  - Measurements: clippings oven-dried at 80°C for biomass; soil pH (H2O); soil moisture via theta probe; bryophyte and vascular plant identifications; biomass and species data sorted by treatment and year.
- Data processing and analyses
  - Biomass data ln-transformed; ANOVA (split-plot Genstat) to test treatment and year effects and their interaction (Table 1; Figure 2c).
  - Normalisation of biomass against Control 1 for cross-year comparisons (Figure 2b).
  - Principal Components Analysis on point-analysis species data (Figure 5); ranking of species before PCA to emphasize treatment differences (Figure 5a–b).
  - Shannon diversity index calculated across surveys to assess changes in diversity over time (Figure 8).
  - Functional-group classification (stress tolerant S; competitive-stress-ruderal CSR; SR/CSR) to interpret community responses (Table 2; Figure 9).
- Data completeness and caveats
  - 2002 included missing periods due to a weather-station malfunction; data for missing intervals substituted from nearby Konza station; overall, some weeks of 2002 data were lost.
  - Biomass and point-analysis data show clear treatment effects and year-to-year dynamics but with notable site-level mowing effects independent of some treatments.

## Data governance, quality and sharing

- Provenance and structure
  - Clear documentation of site layout, block/plot/sub-plot design, and treatment assignments enabling longitudinal linkage of datasets (Appendix 1–2).
  - Multiple data streams integrated to assess productivity, composition, and diversity (biomass, point analysis, soil chemistry, moisture, weather).
- Metadata and standards
  - Treatments labeled consistently (Control 1/2, Nitrogen, Lime, N&L, Insecticide); units and measurement protocols described (Appendix 2; main text).
  - Taxa coding aligned with species lists; functional-type categorization (S, CSR, SR/CSR) used in analyses (Figure 9; Table 2).
- Data quality and QA
  - Use of standardized sampling (0.5 m2 cells; 100-point grids) and consistent mowing regime across years.
  - Statistical treatment of data (ANOVA, PCA, LSD tests) documented; normalisation to control plots facilitates cross-year comparisons.
  - Documentation of anomalies (2002 weather data loss) with transparent substitution strategy.
- Data availability and sharing
  - Primary findings and detailed datasets are documented in the main text and Appendices; detailed datasets and project-specific data are available from project PIs.
  - Soil Biodiversity website referenced as a broader data/resource hub; data accessibility and licensing not explicitly stated; recommended to publish a formal data package with metadata, taxon dictionaries, and treatment maps.
- Data management recommendations for Data Stewards
  - Establish a formal data dictionary covering all measurements, units, codes (plots, blocks, treatments, species codes), and their valid ranges.
  - Maintain versioned data packages with raw vs processed data; track transformations (e.g., biomass normalization, ln-transformations).
  - Create crosswalks for plot-level identifiers (Block, Plot, Sub-Plot, Cell) and treatment labels; standardize taxon nomenclature and CSR classifications.
  - Archive datasets with clear provenance, including dates of collection, methods, and any substitutions for missing data; document any data gaps.
  - Define a data-sharing plan: publish data and documentation (with DOIs/persistent identifiers) in a centralized repository (e.g., Soil Biodiversity site) with licensing and usage terms; provide data dictionaries and method metadata to enable re-use and reproducibility.

## Key findings (condensed)

- Mowing effects
  - Reduction in Agrostis capillaris and Agrostis vinealis across years; moss expansion (bryophytes) linked to reduced disturbance and sward height around 6 cm.
- Fertilisation effects
  - Nitrogen and lime increase productivity; highest productivity in plots receiving both N and lime; pH rises toward 7.0 in lime-treated plots; potential moisture stress in high-pH plots under drought.
  - Functional-shift: increased competitive-stress-ruderal (CSR) and CS-R species in N+L plots; stress-tolerant species flourish in unimproved plots.
- Insecticide effects
  - Higher plant diversity in insecticide plots; possible link to reduced herbivory allowing palatable species to persist; causality requires cautious interpretation due to lack of direct insecticide impact measurements.
- Trampling effects
  - 2002 C2 plots show reduced productivity, likely due to trampling during intensified sampling/13CO2 pulse activities.
- Biodiversity and functional structure
  - Long-term shifts toward stress-tolerant and CSR groups in fertilised plots; bryophyte abundance increasing across the site, especially in unimproved treatments.
  - PCA and diversity indices show clear divergence between improved (fertilised) vs unimproved plots, with bryophyte and certain grasses contributing to the shift.

## Practical takeaways for Data Stewards

- Plan for robust longitudinal data governance across multi-year, multi-stream field experiments.
- Maintain comprehensive metadata for treatments, blocks, plots, subsamples, dates, and methods; align taxon and functional-type coding across datasets.
- Implement data QA workflows, document data cleaning and transformation steps, and preserve raw vs processed data with clear versioning.
- Address and document data gaps (e.g., 2002 weather data loss) with transparent imputation or substitution notes.
- Prepare data packages for sharing with clear data dictionaries, taxon mappings, and method metadata; consider DOIs and open licenses to facilitate reuse.
- Ensure interoperability across data streams (biomass, soil chemistry, vegetation surveys, weather) and maintain consistent units and coding schemes for easy integration and downstream analysis.
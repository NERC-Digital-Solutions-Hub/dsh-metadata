# AFEX Experiment

## Overview
- Location: AFEX project area within the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Brazil (coordinates 02°25'00"S, 59°43'00"W).
- Environment: Plateaued terrain (80–160 m above sea level) with steep slopes and valleys; climate with little seasonal temperature variation; mean annual rainfall 1900–3500 mm, peak rains in April, dry period June–October; relative humidity 75–92% during the year.
  
## Experimental design
- Type: Full factorial nutrient addition experiment.
- Treatments: Eight treatments including untreated control and combinations of nitrogen (N), phosphorus (P), and cations (K, Mg, Ca) in various combinations (N, P, Cations, N+P, N+Cations, P+Cations, N+P+Cations).
- Replication and layout: Four replicates per treatment across four independent blocks (at least 250 m apart), totaling 32 plots.
- Plot dimensions: Each plot 50 m × 50 m; central sampling area 30 m × 30 m to maximize litter from trees within plots.
- Nutrient application: Dry granular nutrients applied to soil surface three times per year with annual rates:
  - N: 125 kg ha^-1 yr^-1 (as urea)
  - P: 50 kg ha^-1 yr^-1 (as triple superphosphate)
  - Ca: 50 kg ha^-1 yr^-1
  - Mg: 20 kg ha^-1 yr^-1 (as dolomitic limestone)
  - K: 50 kg ha^-1 yr^-1 (as potassium chloride)

## Measurement of leaf area loss by herbivory
- Sampling: Litter from all treatments collected and scanned to determine area (m^2) using flat leaves suitable for field scanning.
- Imaging: Leaf images captured with a Canon CanoScan LiDE 120 scanner.
- timing: Analyses conducted in August of 2017, 2018, and 2019 (peak litterfall), with a subset of leaves from all littertraps per plot analyzed each year (total of 160 littertraps).
- Analysis: Leaf area and area lost quantified using ImageJ; processing included gap filling to estimate leaf area without herbivory and hence herbivory area.
  
## Data management and structure
- Data collection approach: Leaves scanned and analyzed to estimate herbivory, with central emphasis on ensuring that measurements reflect representative annual herbivory.
- Data spreadsheet (example columns and meanings):
  - Column A: N (number)
  - Column B: TRT (treatment: 7 treatments plus Control)
  - Column C: PlotID (Block–Plot; e.g., 1–8)
  - Column D: Year (collection year)
  - Column E: Month (collection month)
  - Column F: Leaf_area_mm (mean leaf area measured on herbivory leaves, in mm^2)
  - Column G: Leaf_filled_area_mm (mean area projected without herbivory, in mm^2)
  - Column H: LMA_gm2 (Leaf Mass per Area; g m^-2)
- Outputs: Combined results provide an overall estimate of herbivory across years, enabling comparison among treatments and blocks.
  
## References
- Araújo, A. C., et al. 2002. Comparative measurements of CO2 fluxes from two towers at Manaus LBA site.
- Laurance, W. F., et al. 2018. An Amazonian rainforest and its fragments as a laboratory of global change.
- Metcalfe, D. B. 2014. Herbivory contributions to ecosystem carbon and nutrient cycling in tropical forests.
- Witkowski, E. T. F., & Lamont, B. B. 1991. Leaf specific mass confounds leaf density and thickness.

## Relevance to environmental health monitoring and framework challenges
- Demonstrates a structured, transparent approach to measuring a key ecological health indicator (herbivory impact on leaf area) within a nutrient manipulation experiment, supporting assessment of ecosystem responses to nutrient inputs.
- Data are organized with explicit metadata (treatment, plot, year, month) and clearly defined measurements (area metrics, LMA), facilitating data governance, reuse, and cross-study comparability.
- Reflects practical data collection and processing steps (field sampling, digital imaging, and standardized analysis), addressing common monitoring challenges such as data availability, metadata completeness, and the need for data transformation and quality assurance.
- The design emphasizes replication, blocking, and central sampling areas to improve data reliability and reduce biases, aligning with best practices for monitoring programs seeking policy-relevant insights.
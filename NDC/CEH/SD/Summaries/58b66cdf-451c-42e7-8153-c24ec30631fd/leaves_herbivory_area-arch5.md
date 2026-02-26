# AFEX Experiment

## Overview
- Location: AFEX project area, Biological Dynamics of Forest Fragments Project (BDFFP/INPA), about 80 km north of Manaus, Brazil (02°25' S, 59°43' W).
- Climate/Environment: Tropical Amazon region with limited seasonal temperature variation; average ~26.7°C; mean annual rainfall 1900–3500 mm (peak rainfall in April, dry period Jun–Oct); relative humidity 75–92%.
- Study purpose: Full factorial nutrient addition experiment to assess ecosystem responses to nitrogen (N), phosphorus (P), and cations (K, Mg, Ca) additions and their combinations; includes an untreated control.
- Experimental design: Eight treatments (Control + all single and combination nutrient additions) across 4 independent blocks, 32 plots total (50 m x 50 m each), with 30 m x 30 m central measurement area per plot; plots dispersed on a plateau with at least 250 m between blocks and 50 m between plots.

## Data Assets and Structure

- Primary data focus: Leaf area lost to herbivory, collected as litter samples from all treatments.
- Sampling and timing: Litter collected and leaves scanned in August 2017, 2018, and 2019 (peak litterfall); 160 littertraps sampled across plots.
- Data processing: Leaf area measured from scanned leaves using ImageJ; gap-filling used to estimate non-herbivory area for comparison.
- Data spreadsheet schema (Columns A–H):
  - N: Sample number
  - TRT: Treatment code (7 treatments + Control)
  - PlotID: Block and Plot identifiers for littertrap locations
  - Year: Year of collection
  - Month: Month of collection
  - Leaf_area_mm: Mean herbivore-affected leaf area (mm^2)
  - Leaf_filled_area_mm: Mean leaf area after gap-filling to represent non-herbivory area (mm^2)
  - LMA_gm2: Leaf Mass per Area (g m^-2)
- Data collection instrument: Canon CanoScan LiDE 120 scanner; ImageJ for analysis.

## Experimental Design Details

- Treatments and replication: 8 treatments (Control, N, P, cations, and all combinations) with 4 blocks, totaling 32 plots.
- Plot layout: Each plot 50 m x 50 m; central 30 m x 30 m area used for measurements to maximize likelihood that sampled litter originated from within plots.
- Nutrient application rates (annual): N 125 kg ha^-1 year^-1 (urea), P 50 kg ha^-1 year^-1 (triple superphosphate), Ca 50 kg ha^-1 year^-1, Mg 20 kg ha^-1 year^-1 (dolomitic limestone), K 50 kg ha^-1 year^-1 (potassium chloride).

## Methods and Data Processing

- Leaf area assessment: Images processed to estimate leaf area and herbivory; non-herbivory area inferred via gap filling to standardize comparisons.
- Temporal and spatial alignment: Year and Month fields standardize collection timing across plots and treatments.
- Documentation of methods: Links to established protocols (e.g., leaf area analysis, herbivory measurement) and field collection procedures.

## Data Quality, Provenance, and Documentation

- Provenance: Detailed description of experimental setup and data collection timing provided.
- Metadata considerations for data governance:
  - Clear definitions of units (mm^2 for leaf area; g m^-2 for LMA)
  - Standardized treatment coding (TRT) and plot identifiers (PlotID)
  - Mapping between Block, Plot, and littertrap locations
- Quality checks to consider:
  - Consistency between Leaf_area_mm and Leaf_filled_area_mm
  - Verification of Year/Month accuracy and alignment with sampling events
  - Validation of LMA calculations and unit consistency

## Sharing, Access, and Reuse Considerations

- Data format: Spreadsheet with columns A–H; consider developing a formal data dictionary and a schema for interoperability.
- Documentation needs: Comprehensive metadata detailing experimental design, treatment mappings, plot layout, sampling schedule, and methods (scanner, ImageJ processing, gap-filling).
- Access considerations: Not specified in the text; document potential embargoes or restrictions if applicable.
- Reuse potential: Enables analysis of herbivory contributions to carbon and nutrient cycling under varied nutrient addition scenarios in tropical forests.

## Data Stewardship Challenges

- Incomplete understanding of user needs and priorities.
- Ensuring timely reception of data from multiple data creators.
- Achieving consistent metadata and data standards across contributors.
- Managing data across different systems and formats.
- Handling larger datasets and potential transfer issues.
- Dealing with outdated databases that may require custom, non-interoperable solutions.

## References and Context

- Site climate and context references:
  - Araújo et al. 2002 on CO2 flux measurements at Manaus LBA site
  - Laurance et al. 2018 on Amazon rainforest fragments as a laboratory of global change
  - Metcalfe 2014 on herbivory and ecosystem carbon/nutrient cycling
  - Witkowski & Lamont 1991 on leaf area measurements and gap filling considerations
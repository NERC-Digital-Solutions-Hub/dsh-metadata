# Experimental Field Sites.

## Overview
- Study location: Climate Match tree diversity experiment in the UK, across two sites – Hucking (Kent) and Hartshorne (Derbyshire).
- Focus: Oak (Quercus robur) data on insect herbivores and powdery mildew, within a larger multi-species provenance experiment.
- Temporal scope: Data collected in 2016 and 2017 (powdery mildew and herbivory measurements; height/apparency measured in August 2017).
- Experimental context: Part of TreeDivNet, with predefined provenance and mixture treatments across plots and blocks.
- Purpose for data stewards: Documentation of provenance, treatments, sampling design, and measured variables to support discovery, governance, and reuse.

## Study design and provenance/treatments
- Plantings: Two sites with three experimental blocks per site; treatments replicated once per block for each tree species.
- Provenance and treatments for oak (Quercus robur): 
  - Monocultures of Local, French, Italian provenances.
  - 50:50 and 75:25 mixtures of Local with French or Italian provenances.
  - 33:33:33 mixture of Local, French, Italian provenances.
  - Mixed species plots containing Local and Italian provenances.
- Plot dimensions:
  - Monocultures and mixed-provenance plots: 12 m x 12 m (36 trees per plot).
  - Mixed-species plots: 36 m x 32 m (288 trees total).
- Sampling scope: Nine oak trees per provenance per plot selected for recording, with outward plotting from plot core.

## Data collected and measurements
- Powdery mildew (oak powdery mildew):
  - Collected in August (2016 at Hucking; 2017 at both sites for Hucking and Hartshorne).
  - Sampling: 10 lammas shoots per tree; from all aspects/heights.
  - Severity scoring: 0–3 scale based on percentage of leaf material infected.
  - Covariate: Lammas shoot length (mm).
- Insect herbivores:
  - Collected in August (2016 at Hucking; 2017 at both sites for Hucking and Hartshorne).
  - Sampling: 10 primary shoots per tree; counts of leaf mines, galls, and incidences of leaf skeletonisers/rollers/webbers.
  - Covariate: Primary shoot length (mm).
- Tree height and apparency:
  - Height measured at end of August 2017 for focal trees and 27 additional random trees per plot.
  - Apparency index calculated as: ( focal tree height − plot average height ) / plot average height × 100.
- Additional data captured:
  - PShootLength: Mean primary shoot length (mm) across 10 shoots per tree.
  - LShootLength: Mean lammas shoot length (mm).
  - LShootPM: Mean mildew score on lammas shoots (0–3) averaged across 10 lammas shoots.
  - Leaf.Manip, Leaf.Gallers, Leaf.Miners: Totals across all 10 shoots per tree.
  - TreeHeight: Focal tree height (cm).
  - MeanHeight: Average height of a randomised sample of 28 trees per plot (including focal tree) (cm).
  - Apparency: Plot-level apparency index (as defined above) (%).
- Taxon and provenance metadata:
  - Site, Year, Provenance (coded values), Block, Plot, Treatment, Tree Number.
  - Species focus: Quercus robur across multiple provenance treatments.

## Data structure (nature and units)
- Data frame columns:
  - Site (Hartshorne or Hucking)
  - Year (2016 or 2017)
  - Provenance (codes such as Local_UK2404, UK provenance region 404, Local_Kent, French, Italy_Tuscany, Italy Ravenna)
  - Block (experimental block within site)
  - Plot (experimental plot within block)
  - Treatment (provenance/mixture treatment code)
  - Tree Number (within plot)
  - PShootLength (mean primary shoot length in mm)
  - LShootLength (mean lammas shoot length in mm)
  - LShootPM (mean oak powdery mildew score on lammas shoots; 0–3)
  - Leaf.Manip (sum total of leaf manipulators across 10 shoots)
  - Leaf.Gallers (sum total of leaf gallers across 10 shoots)
  - Leaf.Miners (sum total of leaf miners across 10 shoots)
  - TreeHeight (height in cm)
  - MeanHeight (mean height of 28-tree sample per plot in cm)
  - Apparency (percentage apparency index)
- Additional context:
  - Yearly and site-specific data availability (e.g., Hartshorne 2017 data only; Hucking 2016 and 2017 data).

## Data quality, limitations and governance
- Sampling and mortality:
  - Tree counts varied by year/site due to mortality (e.g., differences in between-year tree totals at Hucking).
- Measurement limitations:
  - Powdery mildew identification is based on visual scoring without molecular confirmation; term “powdery mildew” represents a complex of Erysiphe species.
  - Insect herbivore data are counts per shoot; potential observer bias in counting across leaves.
- Provenance and metadata considerations:
  - Provenance codes are essential for data discovery and reproducibility; ensure consistent interpretation across datasets.
  - Geographic coordinates for sites are provided; coordinate precision is important for mapping and cross-study integration.
- Interoperability:
  - Data are specific to oak hosts within a broader TreeDivNet framework; cross-dataset harmonisation may require careful mapping of provenance codes and treatment labels.

## Access, provenance and references
- Data context: Part of TreeDivNet network; dataset aligns with Barsoum (2015) provenance/mixing design and related oak disease and herbivory literature.
- Key references for metadata interpretation and methodology:
  - Barsoum (2015) – Mixed provenance and mixed species trials.
  - Ayres & Edwards (1982); Marçais et al. (2014, 2009, 2018); Desprez-Loustau et al. (2018) – powdery mildew and oak-pathogen interactions.
  - Sinclair et al. (2015); Moore et al. (1991) – herbivory measurement approaches.
  - Castagneyrol et al. (2018) – apparency index methodology.
- Data stewardship notes:
  - Ensure metadata captures Site, Year, Provenance, Block, Plot, Treatment, and measurement definitions.
  - Maintain explicit data dictionary and units (mm for lengths, 0–3 scale for mildew, counts for herbivores).
  - Document any data updates, corrections, or re-scoring, and link to the TreeDivNet data portal or repository.
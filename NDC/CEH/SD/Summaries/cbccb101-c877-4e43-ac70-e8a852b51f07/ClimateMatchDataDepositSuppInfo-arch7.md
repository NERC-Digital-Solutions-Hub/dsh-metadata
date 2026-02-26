# Experimental Field Sites

## Overview
- Study conducted at the Climate Match tree diversity experiment sites in the UK (2011 planting).
- Sites: Hucking, Kent (51°17'47.5"N, 0°37'58.2"E) and Hartshorne, Derbyshire (52°47'41.1"N, 1°30'58.8"W).
- Focus on Quercus robur (oak) with diverse provenance treatments; part of the TreeDivNet international network.
- Data support GIS-based analysis of spatial patterns in herbivory and disease across provenance and mixture treatments.

## Study System and Timing
- Targeted insect guilds on oak: cynipid gallwasps (gallers), leaf miners, and leaf manipulators.
- Pathogen: oak powdery mildew (Erysiphe spp.), with emphasis on E. alphitoides in the UK context.
- Temporal pattern: herbivory mainly on primary shoots in spring; powdery mildew on lammas shoots in early-to-mid summer; infection distinguished by shoot flushes.

## Experimental Design and Provenances
- Three experimental blocks per site; plots designed for monocultures and mixtures.
- Treatments include:
  - Mono: monoculture of a single provenance.
  - P1P2_50 / P1P2_75: 50:50 or 75:25 mixes Local-French or Local-Italian.
  - P1P3_50 / P1P3_75: 50:50 or 75:25 mixes Local-Italian.
  - 33:33:33: three-provenance mix (Local, French, Italian).
  - MixSp: mixed species plots containing Local and Italian provenances of each species.
- Plot sizes: 12 m x 12 m for provenance monocultures and mixed-provenance plots; 36 m x 32 m for mixed-species plots (288 trees per plot).
- Nine oak trees per provenance per plot sampled; planting and layout ensure mixed provenances/species with no adjacent duplicates.

## Plot Layout and Sampling
- Sites differ in geographic region; local and climate-matched provenances vary by site.
- Sampling strategy: start at plot core and move outward; 9 trees per provenance per plot recorded for powdery mildew and herbivory.
- Sampling years:
  - Hucking: 2016 and 2017 (powdery mildew and herbivory in August).
  - Hartshorne: 2017 only (powdery mildew and herbivory in August).
- Total trees sampled:
  - Hartshorne: 411 trees.
  - Hucking: 420 trees in 2016 and 416 trees in 2017 (mortality reduced counts in 2017).

## Measurements and Covariates
- Powdery mildew:
  - Assessed on 10 lammas shoots per tree in August.
  - Severity scored 0–3 based on percentage of leaf material infected (0, <50%, 51–75%, 76–100%).
  - Lammas shoot length recorded as a covariate.
- Insect herbivores (on 10 primary shoots per tree):
  - Counts of leaf mines, galls, and incidences of leaf skeletonisers, leaf rollers, and leaf webbers.
  - Primary shoot length recorded as a covariate.
- Tree height and apparency:
  - Final height measured for focal trees; plus 27 random trees per plot measured to compute apparency index.
  - Apparency index formula: (Height_focal - Average_height_plot) / Average_height_plot × 100.

## Data Structure and Variables
- Key fields in the data frame:
  - Site, Year, Provenance, Block, Plot, Treatment, Tree Number
  - PShootLength (mean primary shoot length, mm)
  - LShootLength (mean lammas shoot length, mm)
  - LShootPM (mean lammas shoot powdery mildew score)
  - Leaf.Manip, Leaf.Gallers, Leaf.Miners (abundance totals)
  - TreeHeight (height in cm)
  - MeanHeight (mean height of 28 trees per plot)
  - Apparency (percent apparency index)
- Provenance codes include Local_UK2404, UK_provenance_404, Local_Kent, French, Italy_Tuscany, Italy_Ravenna, among others.
- Data collection sites and years enable spatial analyses of provenance effects, mixture treatments, and host-pathogen/insect interactions.

## Geographic Context and Relevance for GIS
- Precise site coordinates enable spatial mapping of infection and herbivory patterns across plots and treatments.
- Data supports mapping of:
  - Spatial distribution of powdery mildew and insect damage by provenance and treatment.
  - Relationship between tree apparency, height, and damage metrics.
  - Integration with environmental layers (climate, soil, microtopography) within TreeDivNet contexts.
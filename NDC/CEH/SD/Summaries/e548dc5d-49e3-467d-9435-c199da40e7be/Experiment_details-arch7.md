# pigAMRgenecounts.csv

## Overview
- Quantitative PCR (qPCR) read outs of antimicrobial resistance gene (AMRG) assays with metadata from a UK commercial pig unit.
- Output: mean gene copies per microlitre of DNA extract for each sample.
- Sample types: faecal and environmental (sow housing barn, pig growing houses, slurry tanks, and random environmental samples on farm and surrounding land).
- Studies: main study (Oct 19, 2016 – Apr 5, 2017) and a depopulation (depop) study (Jun 19, 2017 – Nov 13, 2017); data generated Aug 1, 2017 – May 1, 2018.
- Purpose: monitor dynamics of AMR gene dynamics in relation to antimicrobial administration and farm management practices (including partial depopulation).

## Study scope, design and sampling regime
- Main study: 329 faecal and environmental samples across a 600-sow farrow-to-finish unit; weekly samples from three pen replicates; background sow barn samples; slurry samples for pooled farm representation.
- Depopulation study: 45 additional samples to track AMR dynamics after depopulation.
- Sampling timeline: main study within production cycle; depop study occurs later in 2017.
- Missing values: present due to absence of material or access constraints; assumed to be missing at random and non-informative for analysis.

## Sample collection, storage and processing
- Collection protocols for:
  - Farrowing crate (piglet and sow faeces).
  - Sow barn (faecal material from accessible areas).
  - Slurry (samples from slats and slurry channels).
  - Weaning/growing/finishing pens (piglet faeces).
- On-site storage: -20°C; transport on dry ice; laboratory storage at -80°C.
- Quality control and handling guidance (PCR water use, biosafety cabinet, sterile consumables, dedicated lab gear, separation from amplified DNA, thawing on wet ice, etc.).

## Laboratory workflow (DNA extraction and quantification)
- DNA extraction: PowerSoil DNA Isolation Kit (MoBio) protocol followed with steps for homogenization, lysis, inhibitor removal, DNA binding and elution.
- Final elution: DNA eluted in Solution C6 and stored; concentrations quantified.

## DNA quantification and sample handling
- DNA quantification: NanoDrop 1000; record DNA concentration, 260/280, 260/230 ratios; blank with elution buffer.
- Aliquoting: five 20 µL aliquots per sample; track aliquots and open handling to prevent contamination.
- Data organization: eluted DNA used for qPCR; concentration normalization considerations noted (e.g., to DM or 16S).

## qPCR methodology and targets
- Instrument: Agilent Mx3005p; absolute quantification using standard curves (cloned plasmids) for targets; triplicate runs; include no-template controls.
- Standards: dilution series from 10^7 to 10^1 copies/µL.
- Reagents: Brilliant III Ultra Fast Mastermix; optimized primer/probe concentrations per target.
- Targets and primer/probe contexts:
  - tetB, ermA, ermB, dfrA1, tetQ, and 16S rRNA gene.
  - Primers and probes listed with fragment sizes (e.g., tetB 206 bp; ermA 190 bp; ermB 90 bp; dfrA1 141 bp; tetQ 162 bp; 16S 194 bp).
- Data handling: triplicate measurements; copy numbers extrapolated from standard curves.

## Processing of data and structure
- Data processing: MxPro software used to compute gene copy numbers; results aligned with sample metadata in Excel.
- Output: pigAMRgenecounts.csv containing mean copies per µL of DNA extract per sample.
- Standardization: data can be standardized by percent dry matter (%DM) or by 16S copy number.

## pigAMRgenecounts.csv: Dataset schema (24 columns)
- Column 1: Shortened sample identifier (S/N)
- Column 2: Sample description (e.g., faeces, soil)
- Column 3: Full sample identifier (Sample ID)
- Column 4: Category of pigs (e.g., sow, piglet)
- Column 5: Date of sampling
- Column 6: Sampling site (e.g., sow barn, growing pen)
- Column 7: DNA box ID
- Column 8: DNA concentration (ng/µL)
- Column 9: Sample wet weight (WW, g)
- Column 10: Sample dry weight (DW, g)
- Column 11: Percentage dry matter (%DM)
- Column 12: Distance from sow barn (relevant to environmental transects)
- Column 13: tetB copies/µL
- Column 14: ermA copies/µL
- Column 15: ermB copies/µL
- Column 16: dfrA1 copies/µL
- Column 17: tetQ copies/µL
- Column 18: 16S copies/µL
- Column 19: Experiment type (main or depopulation)
- Column 20: Sample type (faeces, soil, slurry)
- Column 21: Pig type (sows, mixed, piglets, enviro)
- Column 22: Pig age (e.g., sows, mixed, farrowing, weaning, growing, finishing, enviro)
- Column 23: Pen ID (sow barn, slurry tank, farrowing pens, pens 1-3, or enviro)
- Column 24: Antibiotic used (none, mixed, acidified water, acid.chlortet, chlortet, tylosin)

## GIS relevance and potential applications
- Spatial context: uses sampling site, distance from sow barn, and pen/environment identifiers, enabling spatial visualization within a farm layout.
- GIS use cases:
  - Map spatial distribution and intensity of AMR gene copies across farm zones (sow barn, grow-out houses, slurry areas, environmental transects).
  - Integrate with farm management data (antibiotic usage, depopulation events) to explore correlations between practices and AMR gene abundance.
  - Time-series GIS analyses combining main and depopulation studies to assess temporal dynamics and spatial diffusion on the unit.
- Data preparation for GIS:
  - Normalize data by DM or 16S to compare gene abundance across sample types.
  - Align sample IDs with farm layout coordinates or polygon features representing pen locations and environmental zones.

## Data quality, limitations and considerations for GIS
- Missing values exist but are assumed random and non-informative for analysis.
- Spatial coordinates are not provided; spatial analysis would require mapping samples to farm layout positions (e.g., pen IDs, sampling sites) to create approximate GIS representations.
- Normalization options (DM, 16S) should be considered when comparing across sample types and sites.
- Data originate from a single farm unit; results are context-specific and may not generalize without additional spatially explicit datasets.

## Practical notes and provenance
- qPCR and DNA extraction protocols referenced (PowerSoil DNA Isolation Kit; standard qPCR methodology) with specific protocol details and quality controls described.
- Data intended for integration with broader datasets (e.g., for Environmental and Infectious Disease Information Centre or similar repositories) and linked to metadata for reproducibility.
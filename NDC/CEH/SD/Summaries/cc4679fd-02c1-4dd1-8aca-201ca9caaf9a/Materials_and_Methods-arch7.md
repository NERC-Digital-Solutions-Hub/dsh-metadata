# Materials and Methods for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data.

## Overview
- Describes the experimental design, procedures, and analytical methods used to assess bioavailability and toxicity of nanomaterials in sewage sludge to earthworms (Eisenia fetida).
- compares engineered nanomaterials (ZnO, Ag, TiO2) in sludge against ionic metals, including controls.
- collects data on survival, reproduction (juvenile production), and metal uptake in earthworms, with accompanying soil, porewater, and tissue analyses.

## Experimental design and sludge–soil treatments
- Soil: sandy loam (Woburn, UK) amended with sewage sludge derived from WWTP influent spiked with:
  - ENMs: ZnO (30 nm, uncoated), Ag (50 nm, PVP-coated), TiO2 (≈27 nm).
  - Ionic metals: ZnSO4, AgNO3, and micron-sized TiO2 (ionic/bulk metal sludge).
  - Control: no metals.
- Target concentrations and ratios:
  - Ionic metal treatment: target Zn 1400 mg Zn/kg dry soil; sludge:soil ratio 0.58:0.42 (dry basis); designed to reflect EPA guidelines and biosolids risk assessment references.
  - Spiked mixtures were aged in outdoor lysimeters for six months to create aged soil–sludge mixtures.
- Aged treatments (five):
  - (1) Control soil–sludge (no metal)
  - (2) High-metal ENM soil–sludge
  - (3) High-metal ionic metal soil–sludge
  - (4) Low-metal ENM soil–sludge
  - (5) Low-metal ionic metal soil–sludge
- Additional fully replicated soil control (soil only, no sludge) included to ensure adequate reproduction data per OECD guidelines.

## Earthworm exposure setup
- Replicates and containers:
  - Four replicate containers per soil–sludge treatment (≈300 g dry weight per container).
  - Eight soil controls (≈550 g dry weight each) for comparable volume given differing bulk densities.
- Organisms:
  - Eisenia fetida, groups of ten adults per replicate.
  - Food: manure added to soil-only controls; no food added to sludge treatments (sludge itself provides a food source and exposure route).
- Conditions:
  - Temperature: 20 ± 1 °C
  - Photoperiod: 12:12 h light:dark
  - Pre-exposure preparation: worms rinsed, excess moisture removed, weighed as a batch.
- Testing timeline and measurements:
  - 14 and 28 days: survival and batch weight recorded.
  - 28 days: surviving adults removed; three worms per replicate depurated on filter paper for 24 hours to purge gut contents prior to tissue analysis.
  - 28–56 days: continued incubation to allow cocoons to hatch; juveniles counted at the end of this period.

## Single-compound exposure experiments
- Purpose: compare toxicity of as-synthesised ZnO ENM and PVP-coated Ag ENM with Zn and Ag salts.
- Design: identical procedures to soil–sludge exposures.
- Treatments: ZnO ENM, Ag ENM, Zn(NO3)2, AgNO3 spiked into the same soil (Woburn) at multiple concentrations.
- Duration: 28-day survival test and 56-day reproduction test.
- Tissue analysis: three surviving adults per test were prepared for Zn or Ag concentration measurements.

## Soil porewater extraction
- Rationale: porewater is a key uptake route for ionic metals.
- Method:
  - From each treatment replicate, two soil samples (20 g; 25 g for soil control) were collected after 56 days.
  - Samples saturated to 140% of water holding capacity and equilibrated overnight.
  - Porewater extracted by centrifugation (4000 g) using a modified protocol.
  - For Ag analysis, filtration included CuSO4-treated glass wool to minimize adsorption losses.
  - 5 mL of porewater per replicate subjected to ICP-OES analysis for Zn or Ag; pH measured.

## Chemical analyses and metal determinations
- Total metal digestion:
  - For soil and soil–sludge: ~0.75 g (soil) or 0.5 g (earthworms) digested with 3:1 HCl:HNO3 at 140 °C for 2.5 h.
  - Post-digestion: cooled, filtered through CuSO4-pre-treated filter papers; diluted to 50 mL with 0.5% HNO3.
- Porewater digests:
  - 1 mL porewater digested with 3:1 HCl:HNO3 in microwave system; final volume 50 mL with 1% HCl.
- Analysis:
  - ICP-MS (Perkin Elmer Nexion 300D) for Ag and Zn in soil, porewater, and earthworm tissues.
  - Method performance checks described in Supporting Information; instrument detection limits and precision specified (e.g., Ag detection limit ~0.14 µg/L; 1.4% CoV at 5 µg/L).
- Gut-content correction:
  - Total metal concentrations in earthworms corrected for residual gut soil using aluminum as a proxy for gut contents.
  - Correction method based on linear regression between metal and Al concentrations in worms; significant positive relationships found for Ag or Zn with both ENM and ionic exposures, and corrections applied accordingly.
  - Equation: M_worm_corr = M_worm - m × Al_worm, where m is the slope from regression; separate regressions used per exposure type.

## Data types and outputs
- Biological endpoints:
  - Survival rates at 14 and 28 days.
  - Reproduction: number of juveniles at 56 days.
  - Body burden: total Ag and Zn concentrations in earthworm tissues (corrected for gut residues).
- Chemical endpoints:
  - Total Zn and Ag in soil-sludge media and in porewater.
  - Zn and Ag concentrations in earthworms (tissue).
- Experimental metadata:
  - Treatment type (ENM vs. ionic vs. control), metal load levels (high vs. low), aging status, replicate identifiers, and exposure durations.
- Spatial/operational context (potential GIS relevance):
  - Locations: Rothamsted Research (UK) and soil type (Woburn sandy loam); outdoor lysimeter aging conditions.
  - Although not a GIS-focused study, data could be georeferenced to plot locations, soil types, and sludge sources for spatial analyses of metal bioavailability in soils.

## Relevance and quality considerations for GIS-minded use
- Standardized protocols aligned with OECD guidelines (No. 222) support cross-study comparisons and map-based synthesis.
- Detailed metadata (soil type, sludge composition, aging, treatment replication) enables integration into geospatial data products or environmental risk maps when linked to location-based soil and biosolids datasets.
- Data on metal uptake, porewater concentrations, and reproductive endpoints can inform spatial models of contaminant bioavailability and ecosystem risk in GIS environments.

## References (illustrative)
- Ma et al. 2014; Judy et al. 2015; EPA biosolids risk assessments; related toxicogenomic and environmental studies; OECD Guideline 222; various supporting methodological sources cited in the document.
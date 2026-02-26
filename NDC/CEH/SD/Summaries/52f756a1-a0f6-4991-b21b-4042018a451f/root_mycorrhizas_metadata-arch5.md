# AFEX Experiment

## Site description
- Location: AFEX project area, Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Amazonas, Brazil.
- Climate: mean air temperature ~26 °C; mean annual precipitation ~2,400 mm; relative humidity 75%–92% (August–April rainy season).

## Experimental setup
- Design: full factorial nutrient addition experiment with eight treatments and four replicates per treatment.
- Treatments: Control, N, P, cations (Ca, Mg, K), and combinations N+P, N+cations, N+P+cations.
- Layout: 4 independent blocks, each with 8 plots (total 32 plots); plots are 50 m x 50 m, with 30 m x 30 m central area used for main measurements; >250 m between blocks.
- Nutrient application rates (dry granules, applied to soil surface three times/year): N 125 kg ha^-1 yr^-1 (as urea); P 50 kg ha^-1 yr^-1 (as triple superphosphate); Ca 50 kg ha^-1 yr^-1; Mg 20 kg ha^-1 yr^-1 (as dolomitic limestone); K 50 kg ha^-1 yr^-1 (as potassium chloride).

## Root sampling
- In each plot (n=32), five 12 cm-diameter, 30 cm-deep root-free ingrowth cores installed in August 2017 within the central 30 m x 30 m area.
- Sampling schedule: cores collected every three months; four core replicates per plot and soil depth (0–10 cm and 10–30 cm); time frame used for this study corresponds to November 2017–February 2018 (mid wet season).
- Protocol: manual extraction of fine roots within 60 minutes; root-free soil reinserted into holes; roots washed; cumulative root biomass estimated for 60 minutes and extrapolated to 180 minutes using Michaelis-Menten asymptotic curve.

## Root subsampling and mycorrhizal colonisation
- Subsampling focus: fine roots in the 0–10 cm soil depth; mycorrhizal colonisation assessed on root tips (<1 mm diameter).
- AM colonisation assessment: roots cleaned, scanned, cleared and stained following tropical adaptations of standard protocols; staining with Trypan Blue (0.05%) after clearing with KOH, bleaching with H2O2, and acidification with HCl; microscopy at 40x to quantify colonisation.
- Measurement outcome: percent of total root length colonised by arbuscular mycorrhizal (AM) fungi (including hyphae, arbuscules, vesicles).

## Data and metadata (Spreadsheet details)
- Key fields and descriptions:
  - Block: block installation ID (1–4).
  - Plot: specific block/plot identifier within a block.
  - TRT: nutrient treatment applied to each plot (eight treatments as described above).
  - no_am: percentage of root length not colonised by AM fungi.
  - hyphae: percentage of root length colonised by AM hyphae.
  - hyphae_arbuscule: percentage of root length with AM hyphae and arbuscules (arbuscule structures flagged as applicable).
  - hyphae_vesicle: percentage of root length with AM hyphae and vesicles.
  - hyphae_arb_ves: percentage of root length with AM hyphae, arbuscules, and vesicles.
  - total_col: total percentage of root length colonised by AM structures.
- Notes: Units are percentages; certain fields indicate presence/structure codes (e.g., arbuscule structures).

## References
- Araújo et al. 2002; Brundrett et al. 1984; McCormack et al. 2015; McGonigle et al. 1990; Metcalfe et al. 2007; Wurzburger & Wright 2015. (Methodological and contextual references for AM assessment and root analysis.)

## Data governance considerations for stewardship
- Metadata completeness: ensure block, plot, TRT, depth, sampling date, and measurement methods are captured; include sampling intervals and processing steps (e.g., Michaelis-Menten extrapolation).
- Data standardization: harmonize units (percentages for colonisation metrics; kg ha^-1 yr^-1 for nutrients; cm depths; m^2 units for plots if applicable).
- Provenance and reproducibility: document installation date, plot layout, core installation details, and the exact staining/clearing protocol used.
- Data quality: record calibration/validation steps, replicate handling, and any deviations from the protocol (e.g., adjustments in staining or counting).
- Data sharing readiness: provide a clear data dictionary and mapping to the spreadsheet fields above to facilitate discoverability and reuse by others studying tropical forest below-ground responses and AM symbiosis.
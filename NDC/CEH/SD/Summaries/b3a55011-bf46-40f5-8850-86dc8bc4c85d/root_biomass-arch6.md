# Amazon Fertilization Experiment (AFEX)

- Study location and environmental context
  - Conducted inside the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
  - Local soils are clay-rich Ferrasols; rainfall 1900–2500 mm/year with a pronounced dry season (June–October).
  - Forest structure: Above Ground Biomass (AGB) ~322 ± 54 Mg ha-1 (ind ≥ 10 cm dbh); mean wood density ~0.67 g cm-3; ~280 species (≥10 cm dbh) per hectare.

- Experimental design (AFEX)
  - Full factorial fertilization experiment with eight treatments and four replicates (32 plots) arranged in at least four independent blocks separated by ≥200 m.
  - Plot size: 50 x 50 m, with plots at least 50 m apart; located within KM41 with consistent soil, vegetation, and topography.
  - Fertilization scheme (year 1): 125 kg ha-1 N (urea), 50 kg ha-1 P (triple superphosphate), 50 kg ha-1 K (KCl), plus 50 kg ha-1 Ca and 20 kg ha-1 Mg (dolomitic limestone); treatments include Control, N, P, cations, N+P, N+cations, P+cations, and N+P+cations.
  - Fertilization frequency: annually, split into three applications to reduce leaching and runoff; applications performed by hand across plots (systematic walk).

- Data collection methods (root biomass)
  - Target variable: root biomass of fine roots (<2 mm in diameter).
  - In-growth core method: plastic mesh traps (12 cm diameter, 30 cm depth) installed in five points per plot within central 30 x 30 m area; cores filled with root-free soil at installation.
  - Sampling design: five ingrowth cores per plot, pooled to a composite per plot; samples collected at depths 0–10 cm and 10–30 cm.
  - Processing: roots removed in the field within 60 minutes, cleaned, dried at 60°C to constant weight, and weighed.
  - Temporal aspect: first installation provides stock; subsequent samplings conducted every three months.
  - Sampling timeline:
    - 2017: August and November
    - 2018: February, June, September, December
    - 2019: March, June, September, December
  - Data captured per sample includes: PlotBlock, PlotID, Depth, Time_int (e.g., 0–15, 15–30, 30–45, 45–60 minutes), Time, Time_min, and tot_weight (dry weight in grams).

- Data structure and storage
  - Primary data spreadsheet (root biomass) stored and deposited in the EIDC system.
  - Data columns and schema (example):
    - Column A: Census (sampling number)
    - Column B: PlotID (combination of block and plot codes)
    - Column C: Block (B1, B2, B3, B4)
    - Column D: Plot (P1–P8)
    - Column E: Depth (0–10 cm or 10–30 cm)
    - Column F: Time_int (sampling interval, e.g., 0–15, 15–30, etc.)
    - Column G: Time (sampling time label)
    - Column H: Time_min (15, 30, 45, 60)
    Column I: tot_weight (dry weight in grams)
  - The data capture structure supports longitudinal analyses across plots, blocks, depths, and sampling times.

- Data scope and potential analyses
  - Longitudinal data across 32 plots, 8 treatments, 4 blocks, and two depth strata (0–10 cm, 10–30 cm) over 2017–2019.
  - Enables evaluation of how fertilization treatments influence fine root biomass stock and dynamics, by depth and time, under standardized plot conditions.
  - Data can support creation of self-serve data products and dashboards for comparing treatment effects on root biomass and assisting broader ecological interpretations.

- References
  - Duque et al. 2017; de Oliveira & Mori 1999; Metcalfe et al. 2007; Quesada et al. 2011; Rankin de Merona et al. 1992.
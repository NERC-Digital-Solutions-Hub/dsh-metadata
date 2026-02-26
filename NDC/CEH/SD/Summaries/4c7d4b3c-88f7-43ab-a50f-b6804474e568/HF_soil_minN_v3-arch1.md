# Details of data structure to ' HF_soil_minN.csv '

- Overview
  - Supplement to supporting documentation for data series; pertains to HF_soil_minN.csv.
  - Contains 11 columns and 608 rows.
  - Records soil inorganic nitrogen (NH4-N and NO3-N), plus NO2-N in NO3-N context, along with soil moisture contents, soil pH, and electrical conductivity (EC).
  - Data originate from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).

- Dataset composition
  - Depth: Soil samples collected from 0–10 cm depth using a 1 cm diameter corer.
  - Sampling per plot: 6 samples collected and bulked per plot.
  - Analytical context: Soils extracted with 0.5 M K2SO4 (5 g soil to 25 ml solution); analyses performed for nitrate and ammonium.
  - File structure: 608 rows, 11 columns.

- Column-by-column definitions (units)
  - Date: Date of sampling.
  - N_app: Fertiliser application indicator (1|2|3). 1st & 2nd applications at 90 kg ha-1; 3rd application at 60 kg ha-1.
  - Block: Blocking factor in randomized block design (1–4).
  - Plot: Plot identifier within blocks (1–16).
  - Treatment: Fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control).
  - Soil_NH4_mgNkg: Ammonium concentration; mg NH4-N per kg (dry weight basis).
  - Soil_NO3_mgNkg: Nitrate concentration; mg NO3-N per kg (dry weight basis).
  - moisture_dry: Soil moisture on a dry weight basis; g H2O per g dry soil.
  - moisture_wet: Soil moisture on a wet weight basis; g H2O per g wet soil.
  - pH: Soil pH.
  - EC: Soil electrical conductivity; µS cm-1.

- Sampling and analytical methods
  - Sampling method: 0–10 cm soil via corer; six subsamples per plot bulked.
  - Extraction: 5 g soil with 25 ml 0.5 M K2SO4; shaken 30 minutes at 200 rpm.
  - Nitrogen analyses: Nitrate by colorimetric method (Miranda et al., 2001); ammonium by method (Mulvaney, 1996).
  - Moisture determination: Drying at 105°C for 24 hours.
  - pH and EC: Measured using standard electrodes on 1:2.5 soil to deionised water suspension.

- Experimental design and context
  - Trial design: Randomised block design with 4 blocks (Block 1–4) and 16 plots per block (Plot 1–16).
  - Treatments: Four fertiliser regimes (AN, U, IU, C) corresponding to different N inputs and forms.
  - Data purpose: Enables analysis of fertiliser effects on soil inorganic N species, moisture, pH, and EC across combinations of blocks, plots, and sampling dates within the 2016 grassland trial.
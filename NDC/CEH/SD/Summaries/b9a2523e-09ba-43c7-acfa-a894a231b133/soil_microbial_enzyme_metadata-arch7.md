# AFEX Experiment

- Overview
  - Location: AFEX project area, Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Brazil (02° 25' 00'' S, 59° 43' 00'' W)
  - Climate: mean air temperature ~26 °C; mean annual precipitation ~2,400 mm; relative humidity 75%–92% (rainy season peaks)

- Experimental Design
  - Type: full factorial nutrient addition experiment
  - Treatments: eight treatments — control, N, P, cations (Ca, Mg, K), and combinations N+P, N+cations, N+P+cations
  - Replication and layout: 4 replicates per treatment; 4 independent blocks; 32 plots total
  - Plot layout: each plot 50 m × 50 m; central measurement area 30 m × 30 m; blocks spaced at least 250 m apart
  - Nutrient application rates (yr^-1): N 125 kg ha^-1 (as urea); P 50 kg ha^-1 (as triple superphosphate); Ca 50 kg ha^-1; Mg 20 kg ha^-1 (as dolomitic limestone); K 50 kg ha^-1 (as KCl)
  - Application schedule: three times per year; timing avoids the main dry season

- Soil Sampling
  - Timing: after seven months of nutrient addition (January 2018)
  - Sampling design: three soil cores (diameter 5 cm) within central 30 m × 30 m of each plot
  - Depths: 0–5 cm and 5–10 cm
  - Processing: roots removed, samples composited by depth and plot; subsamples allocated for enzyme assays

- Hydrolytic Enzyme Assays
  - Enzymes measured: BG (β-glucosidase, carbon cycling), NAG (N-acetyl-β-glucosaminidase, nitrogen cycling), PHOS (phosphomonoesterase, phosphorus cycling)
  - Method: microplate fluorimetric assays
  - Procedure: 1 g fresh soil in 100 mM sodium acetate buffer (pH 5.5); 200 µL soil suspension added to 96-well plate with 50 µL of MUF substrates (BG, NAG, PHOS) in triplicate; incubate ~1 h at ~25 °C
  - Measurement: fluorescence at 365 nm excitation / 450 nm emission
  - Output units: nmol MUF g soil dry weight^-1 h^-1
  - Quality controls: standard curves and MUF blanks; multiple analytical replicates per substrate

- Data and Metadata (Spreadsheet Details)
  - Fields
    - Block: block identifier (1–4)
    - Plot: plot identifier within each block (1–8)
    - TRT: nutrient treatment applied (eight categories as above)
    - Depth: soil layer sampled (0–5 cm, 5–10 cm)
    - BG: beta-glucosidase activity (description provided)
    - NAG: N-acetyl-β-glucosaminidase activity (description provided)
    - PHOS: phosphomonoesterase activity (description provided)
  - Purpose: structure data for linking spatial blocks, plots, depths, treatments, and enzyme activities

- References
  - Araújo AC. 2002. Comparative measurements of carbon dioxide fluxes from two nearby towers in a central Amazonian rainforest: The Manaus LBA site. Journal of Geophysical Research 107:2156-2202
  - Kaiser C et al. 2010. Belowground carbon allocation by trees drives seasonal patterns of extracellular enzyme activities by altering microbial community composition in a beech forest soil. New Phytologist 187:843-858

- GIS and Data-Management Considerations for GIS Specialists
  - Spatial design aligns blocks, plots, and central measurement areas for map-based visualization of treatments and sampling effort
  - Data can be organized into layers by depth (0–5 cm vs 5–10 cm) and by enzyme metrics (BG, NAG, PHOS)
  - Linking spatial coordinates with treatment, block, plot, and depth enables spatial analyses of enzyme activity patterns
  - Requires consistent metadata and unit standardization across datasets from multiple sources
  - Potential outputs include thematic maps of enzyme activities by depth and treatment, as well as dashboards comparing treatment effects across blocks and plots
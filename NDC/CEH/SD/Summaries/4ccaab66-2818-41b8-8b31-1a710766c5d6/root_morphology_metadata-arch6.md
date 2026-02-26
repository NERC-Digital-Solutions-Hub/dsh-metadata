# AFEX Experiment at the Biological Dynamics of Forest Fragments Project (BDFFP/INPA)

- Location and climate
  - AFEX project area, BDFFP/INPA, ~80 km north of Manaus, Brazil.
  - Mean air temperature about 26°C; mean annual precipitation ~2,400 mm.
  - Relative humidity 75–92% across seasons.

- Experimental setup
  - Full factorial nutrient addition experiment starting May 2017.
  - Treatments: untreated control; N; P; cations (Ca, Mg, K); and combinations N+P, N+cations, N+P+cations.
  - Design: eight treatments, four replicate plots per treatment; total of 32 plots arranged in four independent blocks with ≥250 m between blocks.
  - Plot layout: each plot 50 m × 50 m; central 30 m × 30 m area used for main measurements.
  - Nutrient application rates (dry granules, surface-applied three times/year):
    - N: 125 kg ha-1 year-1 as urea
    - P: 50 kg ha-1 year-1 as triple superphosphate
    - Ca: 50 kg ha-1 year-1
    - Mg: 20 kg ha-1 year-1 as dolomitic limestone
    - K: 50 kg ha-1 year-1 as potassium chloride

- Root sampling and processing
  - In each plot (n=32), five ingrowth cores: 12 cm diameter, 30 cm deep, root-free, installed August 2017 in central 30 × 30 m area (in 2 cm plastic mesh bags).
  - Sampling schedule: every three months after installation.
  - Core replicates: five per plot, pooled by plot and soil depth (0–10 cm and 10–30 cm), giving 64 samples.
  - Focus period: fine roots produced between Nov 2017 and Feb 2018 (wet season middle).
  - Processing: roots washed; 60 minutes of manual extraction; root-free soil reinserted into holes.
  - Extrapolation: Michaelis–Menten asymptotic curve used to estimate biomass for 180 minutes of sampling (from 60 minutes of sampling).

- Root subsampling and morphology
  - Fine roots (<2 mm diameter) from both depths were subsampled.
  - Drying: roots dried at 60°C to determine dry mass.
  - Morphology measurement: scanning of ~¼ of root biomass per sample at 600 dpi; analyzed with WinRHIZO.
  - Morphological metrics derived:
    - Specific root length (SRL) = root length per unit dry mass (cm g-1)
    - Specific root area (SRA) = root surface area per unit dry mass (cm2 g-1)
    - Root tissue density (RTD) = root dry mass per unit volume (g cm-3)
    - Mean root diameter (mm)

- Data and spreadsheet structure
  - Block: block where plots were installed (1–4)
  - Plot: description combining block and plot (1–4, 1–8)
  - TRT: nutrient treatment applied (eight categories: control, P, N, cations, N+P, N+cations, N+P+cations)
  - Depth: soil layer sampled (0–10 cm, 10–30 cm)
  - root_volume: root volume (cm3)
  - tot_weight: total root dry weight (g)
  - SRL, SRA: as defined above
  - RTD: root tissue density (g cm-3)
  - diameter: mean root diameter (mm)
  - These fields capture data across plots, depths, and time for downstream self-serve analyses and reporting.

- References
  - Araújo AC. 2002. Comparative measurements of CO2 fluxes at Manaus LBA site.
  - Metcalfe DB et al. 2007. A method for extracting plant roots from soil.
  - Metcalfe DB et al. 2008. Effects of water availability on root growth and morphology in Amazon rainforest.
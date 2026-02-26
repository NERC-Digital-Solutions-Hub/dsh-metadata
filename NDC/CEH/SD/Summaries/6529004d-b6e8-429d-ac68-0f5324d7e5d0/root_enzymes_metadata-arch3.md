# AFEX Experiment

- Location and climate
  - Conducted at the AFEX project area within the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Brazil.
  - Climate: mean air temperature ~26°C; mean annual precipitation ~2,400 mm; relative humidity 75–92% (lower in August, higher in April).

- Experimental design
  - Full factorial nutrient addition experiment with eight treatments:
    - Control, N, P, cations (Ca, Mg, K), N+P, N+cations, N+P+cations.
  - Design features: 4 independent blocks; 8 plots per block (total of 32 plots).
  - Plot layout: each plot 50 m × 50 m; central measurement area 30 m × 30 m.
  - Nutrient application: dry granules applied three times per year at specified rates.

- Nutrient application rates
  - Nitrogen (N): 125 kg ha⁻¹ year⁻¹ (as urea)
  - Phosphorus (P): 50 kg ha⁻¹ year⁻¹ (as triple superphosphate)
  - Calcium (Ca): 50 kg ha⁻¹ year⁻¹
  - Magnesium (Mg): 20 kg ha⁻¹ year⁻¹ (as dolomitic limestone)
  - Potassium (K): 50 kg ha⁻¹ year⁻¹

- Root sampling strategy
  - Timeframe: nutrient treatments established May 2017; root sampling executed Aug 2017 onward.
  - Ingrowth cores: five 12 cm-diameter, 30 cm-deep cores per plot placed in central 30 × 30 m area; collections every three months.
  - Sample handling: cores homogenised by plot and by soil depth (0–10 cm and 10–30 cm); only fine roots from Nov 2017–Feb 2018 (wet season) used.
  - Sampling duration and extrapolation: root biomass collected for 60 minutes per interval and extrapolated to 180 minutes using a Michaelis–Menten asymptotic curve.

- Root processing and enzyme assays
  - Fine-root subsampling: roots from both depths (0–10 cm, 10–30 cm) were used.
  - Enzyme of interest: potential root acid phosphomonoesterase (PHOS), measured on root tips (<1 mm) as proxy for phosphorus acquisition activity.
  - Assay method: fluorimetric microplate assay using MUF (Methylumbelliferyl-phosphate) as substrate.
  - Procedure details: ~10 mg fresh weight root tissue incubated with MUF; blanks prepared; reaction terminated with NaOH; fluorescence read at 365 nm/450 nm after 20 minutes; results reported as μmol MUF g⁻¹ dry mass h⁻¹.
  - Quality controls: triplicate subsamples per plot per depth; standard lab conditions (incubation ~25°C).

- Data organization and metadata
  - Spreadsheet schema highlights:
    - Block: 1–4 (identifies installation block)
    - Plot: 1–8 (within each block)
    - TRT: treatment descriptor (eight categories: control, N, P, cations, N+P, N+cations, N+P+cations)
    - Depth: soil layer sampled (0–10 cm; 10–30 cm)
    - PHOS: measured PHOS values (μmol MUF g⁻¹ dry mass h⁻¹)
  - Measurements focused on PHOS per plot and per depth, enabling assessment of nutrient treatment effects on root phosphatase activity across soil layers.

- Analytical approach and references
  - Uses a combination of field sampling, lab enzymatic assays, and time-point extrapolation to estimate root enzyme activity.
  - Core references for methodology include studies on root sampling methods, enzyme assays, and phosphate acquisition strategies in tropical soils (e.g., Metcalfe et al. 2007; Lugli et al. 2019; German et al. 2011; Turner & Romero 2010; McCormack et al. 2015).

- Relevance for monitoring frameworks
  - Demonstrates a structured, multi-factorial approach to monitoring below-ground nutrient processing via root enzyme activity in a long-term nutrient addition experiment.
  - Presents a clear data architecture (block/plot/treatment/depth) and standardized processing pipelines (ingrowth cores, depth-specific root sampling, triplicate enzyme assays) suitable for integration into monitoring dashboards and policy-relevant assessments.
  - Highlights the importance of explicit metadata, replicates, temporal sampling, and transparent calculation/extrapolation methods (e.g., Michaelis–Menten extrapolation) to ensure data quality and comparability across studies and time.
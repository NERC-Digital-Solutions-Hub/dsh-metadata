# ReadMe file for SoilSolutionDataAutumn.csv

- Data origin and context
  - Soil solution chemistry data from control (no urine), artificial sheep urine, and nitrate and glucose treatments.
  - Location: humic gleysol within an unimproved grazing area in the Carneddau mountains, Snowdonia National Park, Wales, UK.
  - Coordinates and elevation: 53°22'N, 3°95'W; 556 m above sea level.
  - Sheep excluded from 15/05/17 to prevent excretal events confounding data.

- Experimental design and treatments
  - Treatments:
    - Control: no urine application.
    - ArtUrine: artificial sheep urine applied in discrete patches (each patch ≈1120 kg N ha-1; 200 mL artificial urine per 100 cm2).
    - RealUrine: real sheep urine treatment (referenced in header as RealUrine).
    - Nitrate and glucose treatment: nitrate and glucose (106 kg N ha-1; 213 kg C ha-1) in a 40 cm × 40 cm square.
  - Application date: 25/10/17.
  - Replication: four replicate treatments inside chambers; successful sampling from at least three out of four replicates (minimum n = 3).

- Sampling method
  - Soil solution sampling with Rhizon® samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing).
  - Samplers inserted at a 45° angle to the soil surface within treatment plots.
  - Samples stored frozen at -20 °C until analysis.

- Data structure and variables
  - Data headers (columns):
    - Date: date of soil sample collection (dd/mm/yyyy)
    - Day: days after treatment application
    - Treatment: Control, ArtUrine, RealUrine
    - Chamber: plot and chamber number
    - Nitrate: mg NO3--N L-1
    - Ammonium: mg NH4+-N L-1
    - DOC: mg C L-1
    - TN: mg N L-1

- Analytical methods and QA
  - Nitrate determination: method of Miranda et al. (2001).
  - Ammonium determination: method of Mulvaney (1996).
  - DOC and total dissolved nitrogen: measured with a Multi N/C 2100S analyser (AnalytikJena).
  - Quality control: analyses conducted against certified reference standards.

- Data provenance and usage notes
  - Authors must be acknowledged if data are reused or reproduced.
  - Potential uses: compare soil solution chemistry across treatments and over time, assess effects of urine and nutrient additions on NO3-, NH4+, DOC, and TN.
  - Data may contain missing values due to variable replication (minimum n = 3) and field sampling constraints.

- References for methods
  - Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
  - Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. pp. 1123-1184.
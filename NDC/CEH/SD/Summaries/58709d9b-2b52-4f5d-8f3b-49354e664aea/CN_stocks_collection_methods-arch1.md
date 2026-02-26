# Soil sampling

- Two soil samples were taken per site using a 4 cm width auger, as deep as possible.  
- Soil passed through a 2 mm sieve to remove stones and roots.  
- Stones retained were weighed to determine the proportion of gravel and chalk flints.  
- Soil cores split into 5 cm depth increments, dried at 80 °C for 48 hours after sieving.  
- Cores stored at 25 °C until ready for processing.  

## Bulk density and gravel adjustment

- Soil weighed and bulk density (BD) calculated as mass/volume.  
- BD adjusted for gravel incursions using: Adjusted BD = unadjusted BD × (1 − %gravel/100).  

## Carbon and nitrogen analysis

- Each depth fraction ground in a ball mill at 25 s⁻¹ for two minutes.  
- Samples treated with 10% HCl to dissolve carbonates from chalk via dropwise addition until effervescence ceases.  
- Samples redried and 10 ± 0.5 mg used for combustion analysis.  
- Analysis performed with an Elementar Vario EL combustion analyser, calibrated with an acetanilide standard (10.45% N, 71.4% C).  
- Carbon and nitrogen stocks calculated for each soil depth using the formula: C_t ha = 100 × (core depth / 100) × corrected bulk density × raw C%; N_t ha similarly with raw N%.  
- CN post acid records carbon-to-nitrogen ratio after carbonate removal.  

## Quality control

- Standards and blanks run every 20 samples on the combustion analyser.  
- 5% analytical replicates included.  

## Data file: Soil_C_budgets_to_depth.csv

- Land Use: Land use type.  
- Site: Site identifier.  
- Replicate: Replicate (1 or 2).  
- Soil level: Where the soil was taken from (top, middle, or bottom of the column).  
- Soil Depth from surface: Depth from surface for each increment (5 cm increments where possible).  
- Core depth: Length of the core (not always possible to cut into 5 cm).  
- Core diameter: Diameter of the auger used.  
- Core volume: Volume (πr²h).  
- Dry wt: Soil weight of this increment.  
- Gravel wt: Weight of stones in soil >2 cm.  
- %gravel: Percentage of the core occupied by gravel.  
- Bulk density with gravel: Mass/volume including gravel.  
- BD corrected for gravel: BD after subtracting gravel fraction (e.g., if gravel 10% and BD 1.2, corrected BD = 1.08).  
- N post acid: Total nitrogen after acid treatment.  
- C post acid: Total carbon after acid treatment.  
- C_t ha: Carbon in tonnes per hectare.  
- N_t ha: Nitrogen in tonnes per hectare.  
- CN post acid: Carbon-to-nitrogen ratio after acid treatment.
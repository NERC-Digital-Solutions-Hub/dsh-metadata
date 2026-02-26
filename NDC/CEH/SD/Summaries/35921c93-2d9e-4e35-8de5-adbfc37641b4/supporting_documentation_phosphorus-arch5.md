# Experimental design:

- Overview
  - Intact soil-turf monoliths from a long-term grassland nutrient manipulation experiment (established 1995) in Wardlow, Peak District National Park, UK.
  - Two grassland soil types: limestone grassland (Calc) and acidic grassland (Acid); distinct soil horizons and depths.
  - Treatments in the field: no treatment (natural P limitation, deionized water), phosphorus addition (P: 35 kg P ha-1 yr-1), nitrogen additions (LN: 35 kg N ha-1 yr-1; HN: 140 kg N ha-1 yr-1).
  - Monoliths (10 per treatment per grassland) excavated and transplanted into mesocosms for controlled conditions.

- Experimental setup
  - Monolith excavation and transplantation
    - Limestone: excavated to 10 cm; acidic: to 20 cm (below main rooting depth); transplanted into polypropylene mesocosm boxes with limestone base for limestone sites.
    - Mesocosms embedded in native soil, fully enclosed sides and base, free draining through mesh voile to prevent particulate loss and root ingrowth/ingrowth.
  - Location and climate
    - Bradfield Environment Laboratory (Peak District) ~390 m asl, within ~20 km of Wardlow; similar climate to field site.
  - CO2 enrichment (eCO2)
    - miniFACE system with five 1.6 m rings and five control rings; each ring (FACE or control) contains one of the four nutrient treatments from each grassland, totaling 8 mesocosms.
    - Target daytime CO2: 600 ppm during daylight hours; ambient ~410 ppm; enrichment 2018–2020.
    - Control provided via sensors and automated regulators; fossil fuel-derived CO2 used.
  - Experimental structure
    - Yearly soil sampling and nutrient treatment regime linked to CO2 treatment; data structured to capture location, grassland type, treatment, CO2 level, and mesocosm position.

- Sampling and laboratory analyses
  - Soil sampling
    - Annual collection in September–October from each mesocosm.
    - Triplicate soil cores (2 cm diameter) from random locations; soil in acid grassland split into A and B horizons.
    - Processing: sieve (10 mm then 2 mm), roots removed; moisture content determined by oven-drying at 105°C.
  - Soil microbial biomass phosphorus (MBP)
    - Determined by chloroform fumigation method (Vance et al. 1987).
    - Procedure: fumigated vs non-fumigated 4 g subsamples; extraction with 0.5 M NaHCO3 (pH 8.5); ICP-OES quantification of P.
    - MBP calculation: difference between fumigated and non-fumigated extracts divided by 0.4 (Brookes et al. 1982).
    - Data notes: one non-fumigated sample missing; some negative MBP values removed from dataset.
  - Other measurements
    - Bulk density (g cm-3) recorded; soil moisture and general nutrient data linked to the same samples.

- Data structure and units
  - Dataset fields and descriptions
    - Location: Mesocosm unique ID; Units: String
    - Year: Numeric
    - Depth: Depth increment of soil profile (0-10 cm, 10-20 cm); Units: String
    - Grass: Grassland type; Units: String (Acid = acidic, Calc = limestone)
    - Treat: Nutrient treatment; Units: String (P, 0N, LN, HN)
    - Pair: Experimental block; Units: Numeric
    - CO2: Level of CO2 enrichment; Units: String (A = ambient, E = eCO2)
    - Position: Position within FACE ring; Units: Numeric
    - Soil_P: Soil extractable phosphorus; Units: Numeric (mg kg-1)
    - MBP: Microbial biomass phosphorus; Units: Numeric (mg kg-1)
    - Bulkdensity: Soil bulk density; Units: Numeric (g cm-3)

- Data quality and limitations
  - Missing data: one non-fumigated sample missing (impacts MBP calculation for that plot); additional MBP values removed due to negative results.
  - Metadata specificity: detailed protocol for soil collection, processing, and MBP determination provided to support reproducibility.
  - Consistency considerations: depth increments fixed (0-10 cm, 10-20 cm) and unit conventions clearly specified.

- Data governance and stewardship considerations for Data Stewards
  - Provenance and metadata
    - Link datasets to field site (Wardlow) and mesocosm location (Bradfield), with exact climate and elevation context.
    - Record field treatment history (P, 0N, LN, HN) and CO2 regime (ambient vs eCO2, 600 ppm target, 2018–2020).
    - Include sampling schedule (annual in September–October) and processing steps (sieving, drying, horizon splitting for Acid grassland).
  - Standards and interoperability
    - Maintain standardized units and depth coding; ensure consistency across horizons (A and B splits in Acid grassland).
    - Use the provided schema for dataset fields to enable cross-study integration (Location, Year, Depth, Grass, Treat, Pair, CO2, Position, Soil_P, MBP, Bulkdensity).
  - Data quality controls
    - Capture and flag missing fumigation data and negative MBP values; document reasons and any imputation or exclusion rules.
    - Validate measurement methods (fumigation protocol, ICP-OES, soil moisture) and instrument specifications.
  - Access, sharing, and documentation
    - Provide clear data dictionaries and method references (Vance et al. 1987; Brookes et al. 1982) to support re-use.
    - Document experimental design details (monolith replication, mesocosm construction, CO2 delivery system) to enable reproducibility and meta-analyses.
  - Caveats and limitations
    - Acknowledge potential biases from missing MBP data and horizon-specific sampling in the Acid grassland.
    - Note the extrapolation limits of mesocosm-based findings to field conditions, given controlled enclosure and drainage setup.

- References
  - Vance, E. D., Brookes, P. C. & Jenkinson, D. S. (1987). Extraction method for soil microbial biomass-C.
  - Brookes, P. C., Powlson, D. S. & Jenkinson, D. S. (1982). Measurement of microbial biomass phosphorus in soil.
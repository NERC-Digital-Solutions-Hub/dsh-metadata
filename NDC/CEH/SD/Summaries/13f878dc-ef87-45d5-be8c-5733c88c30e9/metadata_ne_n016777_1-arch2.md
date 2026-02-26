# Introduction

- Purpose: Description of three datasets and their constituent files, linked to published research on Daphnia and responses to multiple environmental stressors.
- Location and system: Lake Ring, Denmark (52°N region), with sediment cores and historical records guiding environmental and life-history analyses.
- Key themes: Paleolimnological data, chemical exposures (carbamate insecticides, Carbaryl), temperature and resource manipulations, and life-history responses across genotypes/populations.

- Dataset 1 (three CSV files linked to Cambronero et al., 2018, Scientific Reports)
  - Cambronero_etal_Environmental_metadata.csv
    - Sedimentary archive data with radiometrically dated years.
    - Nine columns per year: Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi depth (transparency), total nitrates (TN), total phosphates (TP); Na denotes missing data.
    - Data range for transparency, TN, and TP: 1971–1999.
  - Cambronero_etal_pesticides.csv
    - Insecticides sold in Denmark (1955–2010) with total amounts (tons/year).
    - Highlighted cells indicate carbamate insecticides; Carbaryl is specifically noted in this study.
  - Cambronero_etal_life_history_traits_sr.csv
    - Life-history traits from eight variables per individual/population across three common garden experiments.
    - Columns include: IndividualID, populationID, experimental exposure, mortality, size at maturity, age at maturity, fecundity.
    - Experimental conditions: CGE1 (18°C), CGE2 (18°C with high/low food), CGE3 (18°C/24°C with Carbaryl 4 or 10 μg/L).
    - Temperature setpoints: 18°C and 24°C; food levels: 0.2 mg C/L and 2.4 mg C/L; Carbaryl concentrations: 4 μg/L and 10 μg/L.

- Dataset 2 (three CSV files linked to Cambronero et al., 2018, Molecular Ecology)
  - Cambronero_etal_CTmax_bodysize.csv
    - 22 columns summarizing CTmax (temperature of maximum tolerance) and body size for 30 Daphnia magna genotypes.
    - Data collected under exposure to temperature alone (CGE1) and in combination with food levels (CGE2) or Carbaryl (CGE3).
    - Experimental temperatures: 18°C and 24°C; nutrient levels: 0.2 mg C/L and 2.4 mg C/L; Carbaryl levels: 4 μg/L and 10 μg/L; missing data represented as empty cells.
  - Cambronero_etal_Hb.csv
    - Total haemoglobin content (µmol/L) for the 30 genotypes at control temperature (20°C) and after hyper-thermal stress (30°C).
    - Columns include: genotype ID, population ID, mean Hb content across three replicates, and log2 fold-change between temperatures.
  - Cambronero_etal_HSP_expression.csv
    - 27 columns detailing log2 fold-change in expression of four heat shock proteins (HSP20, HSP60, HSP70, HSP90).
    - Measured under: warming alone, warming with high food limitation, warming with Carbaryl, and corresponding non-warming controls.
    - Missing values indicated by empty cells.

- Dataset 3 (two CSV files linked to Cambronero et al., 2021, Evolutionary Applications)
  - Cambronero_etal_Environmental_data.csv
    - Paleolimnological and historical Lake Ring data, including Carbaryl usage (tons/year) from 1955–2010.
    - LOI measurements and ephippia counts (N. ephippia/m2) following hatch under standardized lab conditions.
    - Na denotes missing data.
  - Cambronero_etal_life_history_traits_eva.csv
    - Individual-level life-history traits by population under a full factorial design.
    - Columns: IndividualID, PopulationID, Experiment, Treatment, mortality (days and event), age at maturity, fecundity, size at maturity.
    - Experimental treatments varied two factors: algae concentration (low 0.2 mg C/L vs high 2.4 mg C/L) and insecticide concentration (low 4 μg/L vs high 10 μg/L).
    - Single-stressor conditions (HA, LA, HI, LI) and pair-stressor combinations (HAHI, HALI, LAHI, LALI).
    - Na denotes missing data.

- Publications linked to the datasets
  - 2018 Scientific Reports: Predictability of the impact of multiple stressors on the keystone species Daphnia.
  - 2018 Molecular Ecology: Evolution of thermal tolerance in multifarious environments.
  - 2021 Evolutionary Applications: Evolutionary mechanisms underpinning fitness response to multiple stressors in Daphnia.

- Analytical and data-management implications for environmental monitoring
  - Data verification, quality assurance, cleaning, and transformation steps across datasets.
  - Use of standardized analytical approaches to derive outputs (e.g., CTmax, Hb, HSP expression, life-history metrics, environmental indicators).
  - Presentation of results in clear formats (reports, maps, charts) and proper data archiving (portals) to ensure accessibility and reusability.
  - Challenges highlighted for analysts: increasing data value through integration with other datasets and enabling broad access to underlying data used for outputs.
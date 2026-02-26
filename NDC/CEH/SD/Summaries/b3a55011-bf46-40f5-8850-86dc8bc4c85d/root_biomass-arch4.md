# Amazon Fertilization Experiment (AFEX)

- The study is conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, about 100 km from Manaus, in central Amazonia, on clay-rich Ferralsols with 1900–2500 mm annual rainfall and a pronounced dry season. Forest metrics include above-ground biomass ~322 Mg ha-1 (≥10 cm DBH) and ~280 tree species per hectare.
- AFEX is a full factorial fertilization experiment established in 2017 to assess nutrient effects on forest dynamics across multiple treatments and blocks.

## Experimental Design

- Treatments: eight fertilization treatments (Control; N; P; cations; N+P; N+cations; P+cations; N+P+cations).
- Replication: four replicates per treatment, totaling 32 plots.
- Blocking: four independent blocks, each at least 200 m apart.
- Plot size and layout: each plot 50 x 50 m, with plots within blocks separated by at least 50 m.
- Fertilization rates (yearly): 125 kg ha-1 N (as urea); 50 kg ha-1 P (as triple superphosphate); 50 kg ha-1 K (as KCl); 50 kg ha-1 Ca; 20 kg ha-1 Mg (as dolomitic limestone).
- Data collection scope: data collected from the fine root biomass across specified depths and times to evaluate nutrient effects on root growth.

## Data Collection and Measurements

- Method: in-growth core technique to estimate fine root biomass.
  - Core design: plastic mesh traps, 12 cm diameter, 30 cm depth.
  - Placement: five cores per plot embedded in the central 30 x 30 m area.
  - Depths sampled: 0–10 cm and 10–30 cm.
  - Sampling protocol: roots sampled by hand in the field for 60 minutes total, split into four 15-minute intervals.
  - Processing: roots cleaned in the field, dried at 60 °C to constant mass, and weighed.
  - Definition: fine roots defined as <2 mm in diameter.
- Stock measurement: the initial installation represents the stock measurement.
- Scheduling: sampling occurred quarterly with specific years/times:
  - 2017: August and November
  - 2018: February, June, September, December
  - 2019: March, June, September, December

## Data Structure and Metadata

- Core dataset: root biomass measurements by plot, block, depth, time interval, and weighing interval.
- Data spreadsheet: a structured dataset deposited in the EIDC system.
- Columns and meaning (as documented):
  - Column A - Census: Sampling number
  - Column B - PlotID: combination of block and plot codes (e.g., B1P1)
  - Column C - Block: experimental block (B1, B2, B3, B4)
  - Column D - Plot: 50 x 50 m plots labeled P1–P8
  - Column E - Depth: soil layer (0–10 cm or 10–30 cm)
  - Column F - Time_int: sampling interval within the 60-minute window (0–15, 15–30, 30–45, 45–60 minutes)
  - Column G - Time: four sampling times
  - Column H - Time_min: corresponding minutes (15, 30, 45, 60)
  - Column I - tot_weight: dry weight (g) of the fine root samples
- Data quality notes:
  - Units standardized to grams for biomass
  - Drying temperature and procedure (60 °C to constant weight) documented
  - Times and depths consistently recorded to enable longitudinal analysis
- Data dictionary and column labels provide a clear mapping between coded plot identifiers and experimental design (blocks, plots, and treatments)

## Data Management, Access, and Use

- Data storage: root biomass dataset deposited in the EIDC (European Data Infrastructure for Environmental and Earth Science Data) system.
- Data stewardship: explicit documentation of sampling times, depths, and processing steps supports provenance and reproducibility.
- Potential uses for data leaders:
  - Integrate root biomass responses with nutrient treatments to assess below-ground ecological responses.
  - Cross-link with above-ground measurements and soil properties to model whole-system nutrient dynamics.
  - Shareable data asset for collaboration within BDFFP networks and broader data communities studying tropical forest nutrient dynamics.

## Schedule and Timeline

- Study initiation: AFEX began in March 2017.
- Data collection cadence: quarterly sampling across 2017–2019, with a total of 14 sampling events across 2017–2019 (2 in 2017; 4 per year in 2018 and 2019).

## References

- Duque et al. 2017; De Oliveira & Mori 1999; Metcalfe et al. 2007; Quesada et al. 2011; Rankin de Merona et al. 1992.
# Experimental design/collection method

- Study origin and design
  - Four laboratory-stock populations from Belgium, sourced from two landscape types: two from woodland (Lauzelle, St. Hubert) and two from agricultural landscapes (Lillois, Hoegaarden).
  - Larvae randomly selected and assigned to two host-plant treatments: control vs drought-stressed.
  - Each laboratory source population contributed equally to both treatment groups.
  - Rearing conducted on potted Poa trivialis hosts in climate-controlled common garden conditions until adult eclosion.

- Sample sizes and monitoring
  - Control group: 178 larvae; drought-stress group: 390 larvae.
  - Each larva tracked for development time and eclosion date.
  - On eclosion, F1 adults weighed and sexed.

- Female reproductive output (F1) data collection
  - On eclosion, 100 females selected (50 woodland-origin, 50 agricultural-origin) and placed individually in cages with a P. trivialis plant (control), a male, and a 10% honey solution.
  - When the first egg was laid, the male was removed.
  - Recorded for each female: total eggs laid, mean egg size, egg hatch proportion, and female longevity.

- Wing data collection
  - After death, wings removed, photographed, and morphometrics measured: forewing and hindwing areas, forewing length, and forewing melanization.

- Data formats and storage
  - Stored as CSV spreadsheets:
    - Life_history_data.csv
    - Female_reproductive_output_data.csv
    - Wing_data.csv

- Data headers and units (per file)
  - Life_history_data.csv
    - Headers include: Description, Population, Landscape, Treatment, ID, Adult_mass (mg), Total_development_time (days), Square_root_Total_devtime, sex (m/f).
    - Notes: empty cells indicate missing data (e.g., due to death).
  - Female_reproductive_output_data.csv
    - Headers include: Population, Description, Landscape, Description, ID, Adult_mass (mg), Mean_egg_size (mm^2), Longevity (days), Number_days_until_1st_egg_laid, Fecundity (total eggs), Arcsine square root_% Eggs hatched, %Eggs hatched.
    - Empty cells indicate missing data.
  - Wing_data.csv
    - Headers include: Population, Description, Landscape, Description, ID, Adult_mass (mg), Total_development_time (days), sex, Wing_loading (mg/mm^2), Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area (mm^2).
    - Empty cells indicate missing data.

- Additional notes
  - Descriptions specify that the population site and landscape refer to the source site in Belgium; treatments refer to drought stress vs control host plant used for larval rearing.
  - Some variables are transformations (e.g., Square_root_Total_devtime, Arcsine square root_% Eggs hatched) to aid analysis.
  - Explicitly documents that missing data can arise from death during the experiment.
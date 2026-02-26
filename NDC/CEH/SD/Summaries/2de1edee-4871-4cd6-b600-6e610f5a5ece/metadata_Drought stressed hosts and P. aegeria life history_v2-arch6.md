# Experimental design/collection method: Life history data

## Overview
- Study of life history traits for newly hatched larvae from four laboratory populations across two Belgian landscape types: two woodland populations (Lauzelle, St. Hubert) and two agricultural populations (Lillois, Hoegaarden).
- Larvae originate from the same lab source per treatment and are reared on potted host plants of P. trivialis under climate room, with two treatment conditions: control and drought-stressed.
- Objective across life stages: development, survival, adult mass, sex, female reproductive output, and wing morphology.

## Experimental design and sampling
- Sample sizes: 178 larvae in control; 390 larvae in drought-stress treatment (expected higher mortality under drought).
- Each laboratory source population contributes equivalent numbers to each treatment.
- Each larva is tracked from egg to adult eclosion.

## Data collection and measurements
- Life history data:
  - Date of eclosion; total development time (egg to adult); square-root transformed development time; adult mass at eclosion; sex.
  - Mean egg-to-adult survival calculated per population.
- Female reproductive output:
  - 100 females (50 woodland-origin, 50 agricultural-origin) placed in individual cages with host plant, a mate, and an artificial sugar solution for oviposition.
  - Measurements per female: total eggs laid; mean egg size; longevity; days until first egg laid; fecundity; hatch success (percent eggs hatched; arcsine square root transform provided).
- Wing data:
  - Post-mortem wing dissection: forewing and hindwing images captured.
  - Measured traits: forewing surface area; hindwing surface area; forewing length; forewing melanization; forewing aspect ratio; total wing area; wing loading.

## Data storage and structure
- Data stored as CSV spreadsheets:
  - Life_history_data.csv
    - Headers: Description; Population; Landscape; Treatment; ID; Adult_mass; Total_development_time; Square_root_Total_devtime; sex
    - Note: empty cells indicate missing data (e.g., mortality).
  - Female_reproductive_output_data.csv
    - Headers: Population; Description; Landscape; Description; Treatment; Description; ID; Description; Adult_mass; Mean_egg_size; Longevity; Number_days_until_first_egg_laid; Fecundity; Arcsine_square_root_% Eggs_hatched; %Eggs_hatched
    - Note: empty cells indicate missing data.
  - Wing_data.csv
    - Headers: Population; Description; Landscape; Treatment; ID; Adult_mass; Total_development_time; sex; Wing_loading; Mean_forewing_Melanin; Mean_FW_aspect_ratio; Total_Wing_area
    - Note: empty cells indicate missing data.

## Metadata and headers
- Each CSV includes descriptive headers to enable cross-population and treatment comparisons.
- Headers specify site (Population/Description), landscape type, treatment, and individual-level measurements (mass, development time, reproduction metrics, and wing morphology).
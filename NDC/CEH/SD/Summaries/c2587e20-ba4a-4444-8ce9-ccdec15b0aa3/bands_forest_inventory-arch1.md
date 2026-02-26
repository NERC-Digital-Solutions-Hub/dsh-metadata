# Amazon Fertilization Experiment (AFEX)

- Study area: BDFFP area, KM41 reserve, ~100 km from Manaus (02o24'S, 59o52'W). Soils are clay-rich Ferrasols (~30% of the Amazon Basin). Annual rainfall 1900–2500 mm with a pronounced dry season (Jun–Oct). Above-ground biomass (ind ≥ 10 cm DBH) ~322 ± 54 Mg ha-1; mean wood density ~0.67 g cm-3; ~280 species (≥10 cm DBH) per hectare.

- Objective context: Overview of a full factorial fertilization experiment aimed at understanding how nutrient additions affect forest structure and growth, supported by detailed, repeated tree measurements.

## Experimental Design

- AFEX is a full factorial experiment with eight treatments and four replicates per treatment, totaling 32 plots arranged in four independent blocks spaced at least 200 meters apart.

- Treatments:
  - Control
  - Nitrogen (N)
  - Phosphorus (P)
  - Cations
  - Nitrogen + Phosphorus (N + P)
  - Nitrogen + Cations (N + cations)
  - Phosphorus + Cations (P + cations)
  - Nitrogen + Phosphorus + Cations (N + P + cations)

- Plot layout: Each plot is 50 x 50 meters; plots within and across blocks are separated by at least 50 meters; all plots share similar soil, vegetation, and topography to reduce confounding variation.

## AFEX 2.0: Plot Delineation

- Plot delineation builds on the AFEX design within the KM41 reserve, illustrating the arrangement of blocks (B1–B4) and plots (P1–P8) and their fertilization treatments.

## Fertilization Regime

- Annual fertilization delivered in three applications to mitigate nutrient loss via leaching and runoff.

- Nutrient dosages per year:
  - Nitrogen: 125 kg ha-1 as urea
  - Phosphorus: 50 kg ha-1 as triple superphosphate
  - Cations: 50 kg ha-1 as KCl, plus 50 kg ha-1 of Ca and 20 kg ha-1 of Mg provided as dolomitic limestone

- Application logistics: Fertilizers spread by hand during systemic walks inside the plots.

## Data Collection Methods

- Forest inventories: Conducted annually from 2017 to 2019.
  - 2017 inventory: June–November (longer due to initial botanical identification)
  - 2018 and 2019 inventories: May
  - Diameter at breast height (DBH) measured at 1.3 m above ground for trees with DBH > 10 cm (some measurements adjusted for buttresses or deformities)
  - Population dynamics: recruitment (new individuals reaching DBH > 10 cm) and mortality recorded

- Dendrometric bands (tree growth): Installed on 1,299 trees to obtain precise growth measures.
  - Measurements: distance in circumference (mm) between a fixed window notch and the upper band end, recorded at multiple dates
  - Measurement schedule: 2018 (April, June–Nov) and 2019 (Jan, Feb, Apr, Jul, Oct); 2020 (Jan)
  - Data quality: measurements avoided during rain due to instrument sensitivity; field staff trained for quality control and data entered in the field to minimize errors

## Data Spreadsheets and Variables

- Forest inventory data spreadsheet
  - Key fields: Block, Plot, PlotID, DBH_2017, DBH_2018, DBH_2019, OBS (status: dead, not found, pendant), MH (height), CR (tree features such as alive, buttress, vine presence, damaged, etc.), DN (damage types), Family, Scientific name, Measurement dates (2017–2019)
  - Purpose: per-individual longitudinal growth and status data across three census years, with taxonomic and plot-level context

- Dendrometric bands data spreadsheet
  - Key fields: Block, Plot, subp_x, subp_Y, Family, Specie, date_band_install, DBH_2017, DBH_2018, DBH_2019, Window_Year_Month (circumference change windows), Date_Meas_Year_Month, Obs_Year_Month
  - Purpose: high-frequency growth measurements via trunk circumference changes across multiple bands and dates, enabling precise growth dynamics analyses

- Data accessibility and storage: All datasets are deposited in the EIDC system (data management and discoverability). Data collection and entry emphasized quality control and field-based recording to ensure data integrity.

## Data Quality, Management, and Access

- Quality assurance: trained staff; field data entered directly in the field to minimize entry errors; avoidance of rain during certain measurements to protect instrument accuracy; cross-checks during collection

- Data provenance: explicit linkage among individual trees, plots, blocks, species, and measurement dates; robust metadata for later discovery and reuse

- Limitations and challenges (implied): potential data gaps due to mortality or missing measurements; logistical challenges of consistent annual sampling in a remote forest setting; handling of complex taxonomic and plot-level metadata

## Potential Analyses and Applications (Analysts’ Perspective)

- Treatment effects: compare growth rates (DBH increments, dendrometric growth) across N, P, cations, and their combinations to identify nutrient limitation patterns and interaction effects

- Growth dynamics: leverage dendrometric band data for high-frequency growth trajectories and seasonality analyses, potentially relating to rainfall or other environmental factors

- Structure and composition: assess changes in species abundance and diversity under different fertilization regimes; relate to initial forest structure (AGB, wood density)

- Variability and scaling: explore how effects vary by block, plot position, and soil characteristics (Ferralsols) to assess scale-dependence and local influences

- Data integration: combine DBH time series with dendrometric growth to derive allometric and biomass-change estimates; propagate measurement uncertainty through analyses

- Data reuse and replication: dataset structure supports replication-based inference and cross-study comparisons within tropical forest fertilization experiments

## References

- Duque A, Mulher Landare, HC, Valencia R, Cardenas D, Davies S, de Oliveira A, Perez AJ, Romero Santos H, Vicentini A. 2017. Insights into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.

- De Oliveira A, Mori SA. 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.

- Quesada, CA, Lloyd, J, Anderson, LO, Fyllas, NM, Schwarz, M, Czimczik, CI. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences, 8:1415-1440.

- Rankin de Merona, JM, Prance, JM, Hutchings, RW, Silva, RM, Rodrigues, WA, Uehling, MA. 1992. Preliminary results of a large scale inventory of upland rainforest in the Central Amazon. Acta Amazonica 22:493-534.
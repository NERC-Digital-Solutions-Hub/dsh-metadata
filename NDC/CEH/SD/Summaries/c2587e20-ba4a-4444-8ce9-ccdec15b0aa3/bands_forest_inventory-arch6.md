# Amazon Fertilization Experiment (AFEX)

## Study area
- Located in the BDFFP area, KM41 reserve, ~100 km from Manaus, Brazil (02o 24'S, 59o52'W).
- Local soils: clay-rich Ferrasols (~30% of the Amazon Basin).
- Rainfall: 1900–2500 mm annually with a pronounced dry season (June–October).
- Forest structure:Above-ground biomass (AGB) ≈ 322 ± 54 Mg ha-1 (ind ≥ 10 cm DBH); mean wood density ≈ 0.67 g cm-3.
- Species richness: ~280 species per hectare (≥ 10 cm DBH).

## Amazon Fertilization Experiment (AFEX) design
- Full factorial fertilization experiment started in March 2017.
- 8 treatments with 4 replicates each, totaling 32 plots arranged in four independent blocks (≥200 m apart).
- Fertilization composition per year: 125 kg ha-1 N (urea), 50 kg ha-1 P (triple superphosphate), 50 kg ha-1 K (KCl), plus 50 kg ha-1 Ca and 20 kg ha-1 Mg (dolomitic limestone).
- Treatments: Control; N; P; cations; N+P; N+cations; P+cations; N+P+cations.
- Plot size: 50 x 50 m, minimum 50 m between plots.
- All plots established in areas with similar soil, vegetation, and topography.
- AFEX 2.0 (plot delineation) includes location maps of blocks and plots.

## Collection methods
- Forest inventories conducted annually from 2017 to 2019.
  - 2017 inventory took longer (June–November) due to species identification.
  - 2018 and 2019 inventories performed in May.
- Tree measurements:
  - DBH measured at 1.3 m height using diameter tape (adjusted for buttresses/deformities when needed).
  - Recruitment (new individuals reaching 10 cm DBH) and mortality recorded.
- Data quality:
  - Staff trained prior to collection; field data entered immediately to reduce errors.
  - Dendrometric bands installed on 1,299 trees for more precise growth measures.
  - Growth measurements collected at intervals (rain avoided due to instrument sensitivity).
  - 2018: data collected in Apr, Jun, Jul, Aug, Sep, Oct, Nov.
  - 2019: data collected in Jan, Feb, Apr, Jul, Oct.
  - 2020: data collected in January.

## Data spreadsheets

### Forest inventory data spreadsheet
- Core identifiers and measurements:
  - TAG: unique individual ID
  - Block: experimental block (B1–B4)
  - Plot: 50 x 50 m plots (P1–P8)
  - PlotID: block+plot code
  - DBH_2017, DBH_2018, DBH_2019: tree diameters in respective inventories
  - OBS: status flags (dead, lost, pendant, etc.)
  - MH: measured height
  - CR: condition flags (alive, buttressed, vine, DAP estimation, anchor tree, missing)
  - DN: damage notes (broken trunk, fallen, inclined, etc.)
  - Family: botanical family
  - Specie: scientific name
  - Date measures: measurement dates for each census
- Structure: nested columns for each census year and quality/observational flags.

### Dendrometric bands data spreadsheet
- Structure:
  - Block, Plot, subp_x, subp_Y: location coordinates within plot
  - number Family, specie: taxonomic grouping and species
  - date_band_install: installation date of the dendrometric bands
  - DBH2017, DBH2018, DBH2019: diameter measurements across time (via band windows)
  - Window_Year_Month and Date_Meas_Year_Month: windows and measurement dates
  - Obs_Year_Month: observations such as tape damage or band positioning issues
- Purpose: capture precise growth dynamics via band window measurements across multiple dates.

## References
- Duque et al. 2017. Insigths into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.
- De Oliveira & Mori 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.
- Quesada et al. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences, 8:1415-1440.
- Rankin de Merona et al. 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica, 22:493-534.

## Data utilization and intended outcomes
- Datasets are organized to support exploration, validation, and re-use by researchers and practitioners.
- Data can be used to analyze fertilization effects on tree growth, diameter expansion, species responses, and community structure under controlled nutrient additions.
- Outputs facilitate self-service analysis, potentially including dashboards and reports that summarize AGB dynamics, species responses, and plot-level nutrient effects.
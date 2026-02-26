# Site description

- Overview: Describes the AFEX nutrient addition experiment within the Biological Dynamics of Forest Fragments Project (BDFFP/INPA) near Manaus, Brazil, including location, climate, experimental design, nutrient applications, analytical methods, and data structure.

## Study location and climate

- Location: AFEX project area, BDFFP/INPA, ~80 km north of Manaus, Brazil.
- Coordinates: 02°25' S, 59°43' W.
- Environment: Plateaus (80–160 m above sea level) with steep slopes and valleys.
- Climate: Relatively small seasonal temperature variation; mean ~26.7°C.
- Rainfall: 1900–3500 mm/year; peak in April (>300 mm/month); dry period June–October (<100 mm/month).
- Humidity: 75%–92% (min Aug, max Apr).

## Experimental design (AFEX Experiment)

- Design: Full factorial nutrient addition experiment.
- Treatments: Untreated control + nitrogen (N), phosphorus (P), cations (K, Mg, Ca) and their combinations (N+P, N+Cations, P+Cations, N+P+Cations) for eight treatments.
- Replication: Four replicates per treatment (4 independent blocks).
- Plots: 32 plots total; plots are 50 m × 50 m.
- Central measurements: Central plot area 30 m × 30 m used for measurements to maximize litter sampling from trees inside plots.
- Plot layout: Blocks spaced at least ~250 m apart.
- Nutrient application schedule: Three annual applications.

## Nutrient application details

- N (urea): 125 kg ha⁻¹ year⁻¹
- P (triple superphosphate): 50 kg ha⁻¹ year⁻¹
- Ca: 50 kg ha⁻¹ year⁻¹
- Mg (as dolomitic limestone): 20 kg ha⁻¹ year⁻¹
- K (potassium chloride): 50 kg ha⁻¹ year⁻¹

## Sampling and chemical analysis

- Sampling period: Litter samples collected in August of 2017, 2018, and 2019.
- Processing: Samples bulked by plot; analyses performed at INPA's soil and plants laboratory.
- Sample types: Leaves and insect frass analyzed separately.
- Macro/micronutrients and cations: Analyzed after dry grinding.
- Methods:
  - Macro/micronutrients, P, and cations: Nitroperchloric digestion (Malavolta et al., 1989) and atomic absorption spectrophotometry for K, Ca, Mg, micromutrients (Anderson & Ingram, 1993).
  - Phosphorus: Colorimetry, quantified spectrophotometrically (Anderson & Ingram, 1993).
  - Carbon and nitrogen: Automatic CHN analyzer (Nelson & Sommers, 1996).
- Species identification: Leaves not identified by species; results represent plot-level means.

## Lignin and cellulose analysis

- Method: Acid detergent fiber (ADF) method with sulfuric acid treatment (Van Soest, 1963; Rowland & Roberts, 1994).
- Process: ADF treatment -> cellulose measured with 72% H2SO4; lignin determined by weight loss on ignition (0–50°C).

## Data structure and dataset columns

- Data tracked by a spreadsheet with fields including:
  - N: Number
  - TRT: Treatment (7 treatments plus Control)
  - PlotID: Block and Plot location (e.g., Block1-Plot1)
  - Year: Year of data collection
  - Month: Month of data collection
  - Zn..mg.kg: Zinc in litterfall leaves (mg/kg)
  - Mn..mg.kg: Manganese in litterfall leaves (mg/kg)
  - Ca..g.kg: Calcium in litterfall leaves (g/kg)
  - Mg..g.kg: Magnesium in litterfall leaves (g/kg)
  - K..g.kg: Potassium in litterfall leaves (g/kg)
  - P..g.kg: Phosphorus in litterfall leaves (g/kg)
  - N.porc: Nitrogen percentage in litterfall leaves
  - C.porc: Carbon percentage in litterfall leaves
  - N..g.kg: Nitrogen content in litterfall leaves (g/kg)
  - C..g.kg: Carbon content in litterfall leaves (g/kg)
  - Hemicell.porc: Hemicellulose percentage
  - Cell.porc: Cellulose percentage
  - Lignin.porc: Lignin percentage

## Data notes and considerations

- Leaves not identified to species; values represent plot-level means.
- Data are organized by plot and block across multiple years, suitable for GIS-based visualization of spatial patterns in litter chemistry and nutrient responses.

## References

- Araújo, A. C., et al. 2002. Comparative measurements of CO2 fluxes from two towers at Manaus LBA site.
- Laurance, W. F., et al. 2018. An Amazonian rainforest and its fragments as a laboratory of global change.
- Metcalfe, D. B. 2014. Herbivory contributes to ecosystem carbon and nutrient cycling in tropical forests.
- Malavolta, E., et al. 1989. Avaliação do estado nutricional das plantas.
- Anderson, J. M.; Ingram, J. S. I. 1993. Tropical soil biology and fertility: methods.
- Van Soest, P.J. 1963. Detergent fiber analysis.
- Rowland, A.P.; Roberts, J.D. 1994. Lignin and cellulose in decomposition studies using acid-detergent fiber methods.
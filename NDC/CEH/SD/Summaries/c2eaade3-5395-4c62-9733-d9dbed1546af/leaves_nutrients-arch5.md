# Site description

- Location and context: AFEX project area within the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), about 80 km north of Manaus, Amazonas, Brazil (02°25' S, 59°43' W).
- Environment: Plateau topography (80–160 m above sea level), with steep slopes and valleys; climate with small seasonal temperature variation (avg ~26.7°C) and high rainfall (1900–3500 mm/year; peak >300 mm/month in April; dry period June–October); relative humidity ranges from ~75% to ~92%.

## Experimental Design (AFEX Experiment)

- Experimental setup: Full factorial nutrient addition experiment initiated in May 2017.
- Treatments: Untreated control plus nutrients applied as nitrogen (N), phosphorus (P), and cations (potassium K, magnesium Mg, calcium Ca), including combinations (N+P, N+Cations, P+Cations, N+P+Cations).
- Replication and layout: Eight treatments with four replicate plots per treatment, distributed across four independent blocks (minimum 250 m apart).
- Plots: Each plot measures 50 m × 50 m; central measurement area 30 m × 30 m to maximize litter sampling from trees within plots.
- Plot and sampling structure: 32 plots in total (4 blocks × 8 plots).

## Treatments and Nutrient Application

- Application rates (per year): N = 125 kg ha⁻¹ (as urea); P = 50 kg ha⁻¹ (as triple superphosphate); Ca = 50 kg ha⁻¹; Mg = 20 kg ha⁻¹ (as dolomitic limestone); K = 50 kg ha⁻¹ (as potassium chloride).
- Application timing: Nutrients added manually three times per year, avoiding the main dry season.

## Data Collection and Laboratory Analyses

- Sampling for chemical analyses: Litter samples bulked by plot from litterfall collected in August 2017, 2018, and 2019.
- Laboratory location: Analyses conducted at INPA's soil and plants lab.
- Sample preparation: Dried samples ground (knife and/or ball mill); leaves and insect frass analysed separately.
- Macro/micronutrients and cations: 
  - Nitrogen, micronutrients, phosphorus, and cations analysed using nitroperchloric digestion (Malavolta et al. 1989).
  - Cations (K, Ca, Mg) and micronutrients measured by atomic absorption spectrophotometry (AAS).
  - Phosphorus determined by colorimetry and spectrophotometry.
  - Carbon and nitrogen contents measured with an automatic CHN analyzer (Nelson and Sommers 1996).
- Leaves: Not identified by species; values represent plot-level means.
- Lignin and cellulose: Determined by the acid detergent fiber (ADF) method with sulfuric acid treatment; lignin assessed by weight loss on ignition (0–50°C).

## Data Structure and Metadata

- Data spreadsheet columns (example structure):
  - N: Number
  - TRT: Treatments (7 treatments plus Control)
  - PlotID: Block and Plot identifiers (1–4 blocks; 1–8 plots per block)
  - Year: Year of data collection
  - Month: Month of data collection
  - Zn..mg.kg: Zinc in litterfall leaves (mg/kg)
  - Mn..mg.kg: Manganese in litterfall leaves (mg/kg)
  - Ca..g.kg.: Calcium in litterfall leaves (g/kg)
  - Mg..g.kg.: Magnesium in litterfall leaves (g/kg)
  - K..g.kg.: Potassium in litterfall leaves (g/kg)
  - P..g.kg.: Phosphorus in litterfall leaves (g/kg)
  - N.porc: Nitrogen in litterfall leaves (%)
  - C.porc: Carbon in litterfall leaves (%)
  - N..g.kg.: Nitrogen in litterfall leaves (g/kg)
  - C..g.kg.: Carbon in litterfall leaves (g/kg)
  - Hemicell.porc: Hemicellulose (%) in litterfall leaves
  - Cell.porc: Cellulose (%) in litterfall leaves
  - Lignin.porc: Lignin (%) in litterfall leaves
- Data characteristics: Multi-year (2017–2019) litterfall data across 32 plots, with central measurement area for litter sampling.

## Data Governance and Sharing Considerations for Data Stewards

- Provenance and organization: Data span multiple years and treatments across a defined plot/block structure; sample processing and analyses are centralized at INPA lab with detailed methods cited.
- Metadata needs: Explicit documentation of treatment codes, plot coordinates, exact sampling dates, and any deviations from protocol would support discoverability and reuse.
- Data standardization: Clear data dictionary (as partially shown by the column definitions) is essential for interoperability; standard units and method references are provided but should be captured in a formal metadata schema.
- Accessibility and updateability: The dataset includes historical measurements (2017–2019); guidance would be needed on updating with new years, linking to environmental covariates, and versioning.
- Gaps to address: Species-level leaf identification is lacking; consider adding species attribution or linking litter data to species-level traits if available for enhanced reuse.

## References

- Araújo, A. C., et al. 2002. Comparative measurements of carbon dioxide fluxes from two nearby towers in a central Amazonian rainforest: The Manaus LBA site. J. Geophys. Res. v. 107, p. 58-1 - 58-20.
- Laurance, W. F., et al. 2018. An Amazonian rainforest and its fragments as a laboratory of global change. Biological Reviews, 93, 223-247.
- Metcalfe, D.B. 2014. Herbivory makes major contributions to ecosystem carbon and nutrient cycling in tropical forests. Ecology Letters, 17: 324-332.
- Malavolta, E., Vitti, G.C., Oliveira, A.S. 1989. Avaliação do estado nutricional das plantas: princípios e aplicações.
- Anderson, J. M., Ingram, J. S. I. 1993. Tropical soil biology and fertility: a handbook of methods. 2nd ed.
- Van Soest, P.J. 1963. Use of detergents in the analysis of fibrous foods. II. A rapid method for the determination of fibre and lignin.
- Rowland, A.P., Roberts, J.D. 1994. Lignin and cellulose fraction in decomposition studies using acid-detergent fiber methods.
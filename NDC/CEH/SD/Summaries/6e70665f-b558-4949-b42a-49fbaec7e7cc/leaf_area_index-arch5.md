# Amazon Fertilization Experiment (AFEX)

## Study area and context

- Located within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
- Soils: clay-rich Ferrasols ( ~30% of the Amazon Basin ).
- Climate: annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
- Forest structure: above-ground biomass (ind ≥ 10 cm dbh) ~322 ± 54 Mg ha-1; mean wood density ~0.67 g cm-3; species richness ~280 species ha-1 (≥10 cm dbh).

## Experimental design (AFEX)

- AFEX is a full factorial fertilization experiment with eight treatments, four replicates per treatment, totaling 32 plots.
- Experimental layout: four independent blocks at least 200 m apart; plots 50 × 50 m, spaced ≥50 m.
- Treatments: Control; Nitrogen (N); Phosphorus (P); cations; N + P; N + cations; P + cations; N + P + cations.
- Plot delineation and location: all plots established in areas with similar soil, vegetation, and topography (KM41).
- Fertilization regime: annually in three applications to mitigate nutrient loss via leaching/runoff.
  - N: 125 kg N ha^-1 year^-1 (urea)
  - P: 50 kg P ha^-1 year^-1 (triple superphosphate)
  - K: 50 kg K ha^-1 year^-1 (KCl)
  - Ca: 160 kg Ca ha^-1 year^-1 (dolomitic limestone)
  - Mg: 160 kg Mg ha^-1 year^-1 (dolomitic limestone)
- AFEX 2.0: updated plot delineation within the KM41 reserve.

## Data collection methods

- LAI measurements collected at 36 points per plot using LAI-2200 C.
- Collection window: 6:00–17:00; data not recorded 12:00–14:00 to avoid direct sun.
- Instrument setup: above-canopy reference with sensor in a clearing; fixed compass orientation (west in morning, east in afternoon); 45° view cap; sensors matched prior to data collection.
- Data processing: LAI values computed with FV2200 software using 5, 4, and 3 rings to cover different zenith-angle ranges.
- Campaigns: data collected in Oct 2017, Mar 2018, Aug 2018, and Oct 2018 within the Central Amazon (Manaus region).

## Data documentation and spreadsheet structure

- Data spreadsheet includes:
  - CENSO: sampling number
  - PlotID: combination of block and plot codes
  - B_Obs: the 36 sampling points
  - Time: time of collection for each measurement
  - LAI_5_rings: LAI computed with 5 rings
  - LAI_4_rings: LAI computed with 4 rings
  - LAI_3_rings: LAI computed with 3 rings
  - Date: campaign date (year_month)
  - coord x: horizontal position within plot (0–50 m, in 10 m steps)
  - coord y: vertical position within plot (0–50 m, in 10 m steps)
- Example dataset described as “leaf area index data spreadsheet deposited in EIDC system” (Figure 4).
- Column-level details:
  - A: Sampling number (CENSO)
  - B: PlotID
  - C: B_Obs (36 points)
  - D: Time (HH:MM:SS)
  - E: LAI_5_rings
  - F: Time
  - G: LAI_4_rings
  - H: Time
  - I: LAI_3_rings
  - J: Date (YYYY_Month)
  - K: coord x
  - L: coord y

## Data governance, sharing, and quality

- Data deposited in the EIDC system with explicit metadata and a clear data schema.
- Standardized collection and processing procedures (e.g., calibration steps, consistent timing, and ring-based LAI calculations) to support reproducibility and interoperability.
- Dataset structure supports linking LAI measurements to treatment assignments and plot locations for downstream analyses.

## References

- Duque A, Mulher Landare, HC, Valencia R, Cardenas D, Davies S, de Oliveira A, Perez AJ, Romero Santos H, Vicentini A. 2017. Insights into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.
- De Oliveira A, Mori SA. 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.
- Quesada, CA, Lloyd, J, Anderson, LO, Fyllas, NM, Schwarz, M, Czimczik, CI. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences, 8:1415-1440.
- Rankin de Merona, J.M., Prance, J.M., Hutchings, R.W., Silva, R.M., Rodrigues, W.A., Uehling, M.A. 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica, 22:493-534.
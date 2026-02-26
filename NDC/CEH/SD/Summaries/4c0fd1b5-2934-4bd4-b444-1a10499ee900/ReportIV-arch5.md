# SUMMARY

- Overview
  - Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders), focusing on above-ground productivity, species composition, and diversity in a manipulated field site.
  - Twenty-four Phase I projects and eight Phase II projects explore soil biota and their links to vascular and non-vascular plants.
  - Site previously grazed; from 1998 onward, fencing stopped grazing and a mowing regime was implemented. Five plot-level treatments (nitrogen and/or lime fertilisers; insecticide) plus two controls (Control 1 and Control 2) were applied to main plots subdivided into sub-plots.
  - Functional traits framing used (CSR framework) to interpret shifts in plant communities under different nutrient, disturbance, and insect herbivore regimes.

- Key aims for data stewardship
  - Document and preserve multi-year, multi-format datasets (biomass, soil chemistry, moisture, weather, plant presence/absence and hits) across plots, blocks, and treatments.
  - Maintain metadata on treatments, mowing dates, fertilizer rates, insecticide applications, and sampling protocols to support cross-year analyses and reuse.
  - Ensure data quality, traceability, and accessibility for researchers investigating productivity, diversity, and functional group shifts.

- Data architecture and collection (Methods)
  - Site: Rigg Foot Experimental Site, Sourhope; 5 replicate blocks; 6 main plots per block; 10 sub-plots; 0.5 m2 sampling cells in S, T, U, V sub-plots.
  - Treatments (plot-level): Control 1, Control 2, Nitrogen, Lime, Nitrogen+Lime, Insecticide (Dursban 4 OPA).
  - Management: monthly mowing May–Sept to ~6 cm; insecticide applied after mowing on Insecticide plots; spring applications of Nitrogen and/or Lime.
  - Data streams and measurements:
    - Weather: on-site Automatic Weather Station (headlines in Appendix 5).
    - Biomass: 0.5 m2 cell samples; 5 summer cuts per year; drying at 80°C and weighing.
    - Baseline and longitudinal plant surveys: June–August 1998 baseline 0.5 m2 quadrat; annual 0.5 m2 point analyses (100-hole grid) in 2000, 2001, 2002; bryophyte identification improved in 2002; Appendix 3 lists species.
    - Soil: pH (0–5 cm, and March/July/August 2002 center-of-plot sampling), moisture (theta probe in 2002).
    - Additional small-scale botanical surveys and biomass samples (Appendices 6–8).
  - Data volume and provenance: 11,621 soil samples collected since start; major field campaigns in 1999–2002; datasets underpin biomass, diversity, and functional-group analyses.

- Results at a glance (highlights relevant to data interpretation)
  - Productivity patterns: overall biomass increased over 1999–2002, with the combination of Nitrogen and Lime giving the highest productivity; Biomass in 2002 generally lower than 2001 across most treatments; Control 2 plots consistently less productive than Control 1 in several years.
  - Soil chemistry and moisture: lime sharply raises soil pH toward ~7.0 in upper soil, nitrogen raises pH more modestly; higher pH tends to accompany lower soil moisture; pH–biomass relationships vary by treatment (positive when considering all plots; nuanced within treatments).
  - Species composition and diversity: improved plots (N and/or Lime) show higher abundances of grasses associated with fertile pastures (Festuca rubra, Poa pratensis), while unimproved plots favor Festuca ovina and Anthoxanthum odoratum; bryophytes (e.g., Rhytidiadelphus squarrosus) increase over time, especially in unimproved plots.
  - Functional groups: three dominant functional groups (stress-tolerators S; C-S-R; SR/C-S-R) account for most hits; by 2002, N+L plots favor CSR and SR/CSR, while unimproved plots favor stress-tolerators; insecticide and lime influence the balance of functional groups.
  - Data interpretation tools used: Principal Components Analysis (PCA) to separate improved vs unimproved plots; ANOVA (split-plot) used to test treatment and year effects on biomass.

- Notable data quality and governance notes
  - 2002 weather data: a malfunction caused missing data during July–August; Konza weather station data were substituted for those dates.
  - Bryophyte identification improved in 2002, yielding richer species lists for bryophytes.
  - Some plots (e.g., C2) had first-time sampling in 2002, affecting productivity comparisons and interpreted as trampling effects during 13CO2 pulse work.

- Data accessibility and documentation
  - Primary datasets and full methods are described in this report; raw/processed data and detailed survey results are available from the Project PIs and CEH.
  - Data and appendices are linked to or accessible via the Soil Biodiversity website and CEH (contact details and links provided in the report).
  - Appendices provide comprehensive datasets: site map and treatments (Appendix 2), species lists (Appendix 3), weather (Appendix 5), biomass by plot (Appendix 6), rank analyses (Appendix 7), and species-hit distributions (Appendix 8).

- Data stewardship implications and recommendations
  - Ensure comprehensive, versioned metadata for each data stream (biomass, soil chemistry, moisture, weather, species hits) including measurement protocols, units, timings, and treatment allocations.
  - Preserve raw vs processed data with clear provenance to support reproducibility of ANOVA, PCA, and CSR-based analyses.
  - Maintain data quality controls to document missing data (e.g., weather gaps) and data substitutions; capture reasons and sources for substitutions.
  - Facilitate long-term accessibility by hosting datasets with stable DOIs or identifiers and providing clear data-use licenses.
  - Align data formats and variable naming across years to improve interoperability for cross-year analyses and meta-studies.
  - Document taxonomic updates and identification levels (e.g., bryophyte identification to species in 2002) to support consistent longitudinal analyses.
  - Consider a data dictionary and schema that mirrors the site design (blocks, plots, sub-plots, sampling cells) to ease downstream analyses and reuse by other researchers.
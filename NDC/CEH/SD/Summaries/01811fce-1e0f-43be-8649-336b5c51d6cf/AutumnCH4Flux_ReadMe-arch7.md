# ReadMe file for AutumnCH4Flux.csv

- Purpose and scope
  - Provides CH4 flux measurements from four treatments (Control, Artificial sheep urine, CandN = nitrate and glucose, and C and N) applied to a humic gleysol in unimproved grazing land in the Carneddau mountains, Snowdonia, Wales, UK.
  - Data designed to support map-based analyses of methane flux responses across treatments and plots over time.

- Location and site context
  - Carneddau mountains, Snowdonia National Park, Wales, UK
  - Elevation: 556 m above sea level
  - Coordinates: 53°22'N, 3°95'W
  - Plot context: grazing land; plots with randomized block experimental design; sheep excluded from 15/05/17 to avoid confounding excreta events

- Experimental design
  - Treatments (n = 4): 
    - Control: no urine application
    - Artificial sheep urine: urine applied in triplicate patches (1120 kg N ha^-1 equivalent in total N across patches; 200 ml per 100 cm^2)
    - CandN: nitrate and glucose at 106 kg N ha^-1 and 213 kg C ha^-1; 1 L applied across a 40 × 40 cm square
  - Treatment timing: applied on 25/10/17
  - Design type: randomized block
  - Monitoring period: 45 days post-treatment

- Measurement system and data collection
  - Instrumentation: automated greenhouse gas monitoring system (QUT) with a SRI 8610 GC
  - Flux sampling: eight measurements per chamber per day (1 h chamber closure; 4 gas samples per closure)
  - Calibration: standard analysed after every fourth gas sample
  - Chamber specifications: basal area 0.25 m^2; chambers 50 cm × 50 cm × 15 cm (L × W × H)
  - Data scope: high-frequency flux data captured during the monitoring period; represents quality-assessed flux values (not raw gas concentrations)

- Data content, structure, and units
  - Time stamps: Timestamp = day/month/year hour:minute (dd/mm/yy hh:mm)
  - Temporal reference: Days = days pre- or post-treatment
  - Flux variables: CH4 fluxes represented in µg CH4-C m^-2 h^-1
  - Columns: B to M represent CH4 flux values; column headers encode treatment and chamber/plot identifiers (e.g., Control, ArtUrine, CandN)
  - Data quality note: data have undergone QA to remove anomalies (e.g., gas peak interference) based on raw files and GC chromatograms

- Data quality, cleaning, and provenance
  - Quality assurance performed by inspecting raw data and chromatograms; anomalous data removed as needed
  - Data included are quality-assessed flux measurements (not raw gas concentration data)

- Usage notes for GIS applications
  - Suitable for creating map-based representations of methane flux by chamber/plot and treatment
  - Spatial linkage: chambers correspond to fixed ground plots; can be mapped as polygons or point locations with CH4 flux attributes
  - Temporal analysis: use Timestamp and Days to plot flux dynamics over time post-treatment
  - Attributes to map/include: treatment type, chamber/plot ID, flux values (µg CH4-C m^-2 h^-1), date/time, days relative to treatment

- Attribution
  - Authors must be acknowledged if data are re-used or reproduced

- Limitations and considerations
  - Data are from a single location and experimental context; extrapolation to other sites should consider local conditions
  - Some columns represent multiple chambers/plots under different treatments; ensure correct interpretation when aggregating or mapping by treatment or time
# Hydraulic head dataset (6 files), details as follows:

- Datasets overview
  - 3 datasets described: Hydraulic head (6 files), Hydraulic Conductivity (6 files), and Porewater chemistry (6 files).
  - Each dataset comprises 6 Excel spreadsheets.
  - Hydraulic head files record water height in metres above OS datum (river stage, bed and bank), with site locations given by OS Grid References at multiple river sites (Ebble, Wylye, Avon, Nadder, Sem).
  - Hydraulic conductivity files provide saturated hydraulic conductivity (Ksat) derived from slug tests (falling/rising head) using HOBO pressure loggers; same site coverage as head data.
  - Porewater chemistry files contain measured chemical parameters from porewater samples collected via piezometers at multiple depths and positions (in-stream and bankside).
  - Site codes and locations include CE, CW, GA, GN, AS, AP with corresponding OS Grid References (e.g., CE: SU05598 25343; CW: ST85779 38053; GA: SU09723 57824; GN: ST92380 27376; AS: ST92346 27381; AP: ST89198 28431).

- Field instrumentation
  - HOBO U20-001-01 data loggers (USA) and Levelogger Edge (Solinst, Canada) used for water level measurements.
  - Manta 2 probes (Eureka Water Probes, USA) mentioned for instrumentation.

- Quality control and data reliability
  - Hydraulic head data corrected for drift (probe movement) using manual piezometer dips performed every 2–4 weeks; drift assumed linear.
  - Slug test data (falling/rising head) used to compute Ksat; repeat tests conducted where possible; replicates included.
  - Comparisons between falling and rising head results provided; data quality notes included.
  - Porewater chemistry methods include in-field sampling, lab analyses with quality controls, and use of certified reference materials; data notes indicate <LOD values and non-analysed entries (na).
  - Quick reference contacts for data queries:
    - Andy Binley (a.binley@lancaster.ac.uk) for Hydraulic head and Saturated Hydraulic Conductivity datasets.
    - Kate Heppell (c.m.heppell@qmul.ac.uk) for Porewater chemistry datasets.

- Data structure and file formats
  - Hydraulic head spreadsheets
    - Columns: date and time (dd/mm/yyyy hh:mm) in column A; subsequent columns contain head data expressed as metres AOD, varying by site instrumentation.
  - Saturated hydraulic conductivity spreadsheets
    - Columns: Piezometer ID, Rising or Falling test, Start date/time (dd/mm/yyyy hh:mm), Ksat (m/s), and quality control comments.
  - Porewater chemistry spreadsheets
    - Columns: Date (dd/mm/yyyy), Site code, Sample type (SW = surface water grab; B = bankside piezometer; Sed = in-stream piezometer in bed sediment), Piezometer cluster (UC = upstream, DC = downstream), Depth of porewater (m), numerous analytes (O2, Fe(II), Cl−, NO3−, SO4^2−, DOC, Al, Ca, Fe, K, Mg, Na, Si, Sr, DIC, CH4, N2O, nitrate as N, phosphate as P, ammonia as N); data may be NA for not analysed or <LOD for below detection limit.
  - Data labeling conventions
    - Piezometers are labeled by site location; in-stream piezometers reside in upstream (UC) and downstream (DC) clusters ~10 m apart.
    - Bank piezometers form triangular clusters on left (LB) and right (RB) banks; secondary labels indicate proximity to UC or DC clusters (1 or 2), with a third location (3) completing the triangle.
    - Bank piezometers’ screen depths approximate river bed depth at the channel center near the piezometer.
    - Porewater sampling tubes extend to screen depth and halfway to the screen.

- Analytical chemistry methods and parameters
  - Field oxygen measurements with Unisense electrode; Fe(II) analyzed by UV spectrophotometry after field fixation.
  - Chloride, nitrate, sulfate by Ion Chromatography (Thermo Dionex) with specified analytical columns and eluent; detection limits and RSDs provided.
  - Major cations (K, Ca, Mg, Na, Sr) and silica measured by ICP-OES (Agilent) with specified detection limits and RSDs; use of Certified Reference Materials noted.
  - Phosphate, ammonia, nitrite by Skalar Auto Analyser; detection limits and CRM accuracy provided.
  - DOC measured by non-purgeable organic carbon method (Skalar Formacs HT) with specified detection limit and accuracy.
  - All methodological notes include data quality considerations and CRM references; queries about porewater chemistry datasets directed to Kate Heppell.

- Site structure and dataset organization
  - Data are structured by site clusters and depths:
    - Upstream cluster (UC) and downstream cluster (DC) in-stream piezometers; ~10 m apart.
    - Bank piezometer clusters on left bank (LB) and right bank (RB) with 1, 2, and 3 secondary labels indicating their relation to UC/DC and positions within bank triangles.
    - Porewater sampling tubes extend to various depths (e.g., 10 cm, 20 cm, 30 cm, 50 cm, 70 cm, 100 cm) in UC/DC piezometers.
  - Each dataset’s spreadsheets maintain consistent structure and labeling to facilitate cross-dataset analysis and self-serve exploration.
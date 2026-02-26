# Data Overview

- The MERLIN project aims to upscale restoration of freshwater ecosystems across Europe by providing a framework for implementing nature-based solutions. This dataset covers the first two years of water quality data from Hare Moss (peatland, Forth catchment) to establish baseline conditions before restoration through a control-intervention design.

- Objective: implement a control-intervention approach to characterise differences in the baseline period prior to restoration.

## Sampling design and sites

- Fortnightly sampling from December 2021 to May 2022 at:
  - Hare Burn downstream of the planned restoration area (initial monitoring site)
  - Black Burn near the Auchencorth Research Facility (control site; monitored since 2006)

- May 2022: two additional Hare Burn sites added upstream and downstream of the restoration area, bringing total to four sites.
  - Hare Burn Upstream (HARE US)
  - Hare Burn Downstream (HARE DS)
  - Black Burn (AUCH)
  - Hare Burn (original downstream site later discontinued)

- August 2022: original Hare Burn site discontinued; continued monitoring at Hare Burn Upstream, Hare Burn Downstream, and Black Burn (three sites).

- Upstream peat extraction upstream of the monitoring area influences dynamics (bank collapsing and sand deposition observed).

- Site coordinates and a map are provided (Table 1, Figure 1).

## In-field collection and sample handling

- Water samples collected from near the middle of the stream using a 60 ml syringe; sample types include total phosphorous (TP), soluble reactive phosphorous (SRP), dissolved organic carbon/total dissolved nitrogen (DOC/TdN), and particulate organic carbon (POC).

- Sampling protocol details:
  - SRP and DOC filtered through 0.45 μm filters into sterile tubes; a spare filtered sample collected for potential future analysis.
  - POC collected unfiltered in a pre-rinsed bottle; filters pre-combusted for POC analysis.
  - Duplicate headspace sampling for dissolved greenhouse gases (GHG) using a two-syringe setup.

- In-field measurements: pH, electrical conductivity, dissolved oxygen (DO), and temperature using a HACH HQ4300 multiparameter meter; instruments calibrated before use.

- Sample storage:
  - TP, SRP, and spare filtered samples frozen at -18°C.
  - DOC and POC samples stored at 4°C and analyzed within about a week.
  - Greenhouse gas samples stored at room temperature until analysis.

- Field collection led by named staff (e.g., Alanna Grant, Toby Roberts, Rebecca McKenzie).

## Laboratory analysis and methods

- DOC and TdN:
  - Analyzed with a Shimadzu TOC-LCPH (NPOC method) after acidification and sparging.
  - Standards and blanks used for QA; repeat measurements used if CV > 2%.

- UV/Vis and SUVA:
  - Absorbance measured between 230–800 nm; SUVA at 254 nm calculated to indicate DOC aromaticity.

- Particulate organic carbon (POC):
  - Sample filtration through pre-combusted GF/F filters; LOI method used with a conversion factor to estimate carbon content.

- Total phosphorus (TP) and soluble reactive phosphorus (SRP):
  - TP: digestion with potassium persulfate; colorimetric post-digestion (phospho-molybdate blue) measured with SEAL AQ2; multiple standards included for calibration.
  - SRP: measured by the same colorimetric method on thawed samples.

- Greenhouse gases (GHG):
  - Dissolved CH4, CO2, and N2O analyzed by GC (Agilent 7890B) with μECD and FID detectors; concentrations reported as ppmv and converted to μg/L using Henry’s law.

## Data structure, columns, and units

- Data are organized with:
  - Site and sampling metadata: Site_name, Site_code, Date, Time
  - Field measurements: pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av
  - DOC/TdN and related metrics: DOC, TdN, C_N, Abs_at_254, SUVA
  - Nutrients and carbon phases: TP, SRP, CH4_C, CO2_C, N2O_N, POC
- Detailed column descriptions and units are provided (Table 3), including decimal places and measurement units (e.g., pH, °C, mg/L, µS/cm, µg/L).

## Dataset completeness and data exclusions

- Not all planned observations were retained due to field and laboratory issues; Table 4 lists excluded data with dates, sites, determinants, and reasons (e.g., below detection limit, missing time, samples not collected, pH probe failure, sample unavailable, instrument faults, suspected contamination, in situ pH measurements taken post-collection).

- Examples of exclusion reasons:
  - Below the limit of detection (N2O-N)
  - Time not recorded
  - Samples not collected (TP, SRP, POC)
  - pH probe not functioning or pH measurements performed in-lab after collection
  - Sample contamination suspected (TP)
  - Abnormally low DOC/TdN or abnormally high TP due to instrument faults

- Acknowledges that field instrument or laboratory analyzer failures caused missed or incorrect observations.

## Data quality, access, and references

- MERLIN is funded as a research and innovation action under the European Commission Horizon 2020 programme (grant No 101036337).

- References include foundational methodological papers for carbon and nutrient analysis and instrumental calibrations cited in the dataset documentation.
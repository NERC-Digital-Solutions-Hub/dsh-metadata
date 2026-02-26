# ReadMe file for SoilSolutionDataAutumn.csv

- This ReadMe describes soil solution chemistry data from an experimental setup in Snowdonia National Park, Wales, UK, with multiple treatments to assess how different inputs affect soil solution composition.

## Overview of the dataset
- Focus: soil solution chemistry under control (no urine), artificial sheep urine, and nitrate+glucose treatments.
- Location: humic gleysol in an unimproved grazing area in the Carneddau mountains, Snowdonia National Park, Wales.
- Elevation and coordinates: 556 m above sea level; 53°22'N, 3°95'W.
- Sample collection method: Rhizon soil solution samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing) inserted at a 45° angle within treatment plots.
- Replication: minimum of three samples per treatment (n ≥ 3) across four replicate treatments; successful sampling achieved in at least three out of four replicates.

## Treatments
- Control: no urine application.
- Artificial sheep urine (ArtUrine): patches applied with an N application rate of 1120 kg N ha-1; 200 ml of artificial urine applied over 100 cm2 per patch.
- Nitrate and glucose: nitrate and glucose applied at 106 kg N ha-1 and 213 kg C ha-1 within a 40 cm × 40 cm square.
- Data header includes a Treatment field with values: Control, ArtUrine (Artificial urine), and RealUrine (real sheep urine treatment); note: the narrative describes Control, Artificial urine, and Nitrate+glucose, creating a potential discrepancy between the narrative and header categories.

## Sampling and storage
- Sampling date: treatments applied on 25/10/17.
- Soil solutions were collected and stored frozen at -20 °C until analysis.
- Date and day fields in the data indicate the collection date and days after treatment application.

## Analytical methods and quality control
- Nitrate (NO3−) analysis: method of Miranda et al. (2001).
- Ammonium (NH4+) analysis: method of Mulvaney (1996).
- Dissolved organic carbon (DOC) and total dissolved nitrogen (TN): measured with a Multi N/C 2100S analyser (AnalytikJena).
- All solutions analysed against certified reference standard solutions.
- Data entries were likely quality assured and transformed as part of standard practice (as described in the aims of typical monitoring datasets).

## Data structure and fields
- Data headers in the file include:
  - Date: date of soil sample collection (dd/mm/yyyy).
  - Day: days after treatment application.
  - Treatment: treatment applied to each plot ('Control', 'ArtUrine', 'RealUrine' or other variants as per header).
  - Chamber: plot and chamber number from which the sample was taken.
  - Nitrate: NO3− concentration in mg NO3−-N L−1.
  - Ammonium: NH4+ concentration in mg NH4+-N L−1.
  - DOC: dissolved organic carbon in mg C L−1.
  - TN: total dissolved nitrogen in mg N L−1.
- References for analytical methods included:
  - Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
  - Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3.

## Data usage, sharing, and governance
- Acknowledgment: Authors must be acknowledged if the data are reused or reproduced.
- Data provenance: samplers, sampling design, and storage indicate careful handling and traceability of samples.
- Note on data accessibility: data are accompanied by metadata and methodological references to facilitate reuse and validation; any reuse should cite the provided references and acknowledge the data source.
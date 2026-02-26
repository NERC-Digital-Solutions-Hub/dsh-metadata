# ReadMe file for SoilSolutionDataAutumn.csv

## Overview
- Describes soil solution chemistry data from an experiment with control, artificial sheep urine, and nitrate+glucose treatments.
- Conducted on humic gleysol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Data include concentrations of nitrate, ammonium, dissolved organic carbon (DOC), and total dissolved nitrogen (TN) collected from Rhizon soil solution samplers.

## Location and experimental design
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Plot setup: Treatments applied inside chambers; sheep excluded from 15/05/17 to minimize confounding excretal events.
- Sampling depth/technique: Rhizon soil solution samplers (2.5 mm diameter, 5 cm porous portion, 12 cm tubing) inserted at a 45° angle relative to the soil surface, within the treatment plots and chambers.
- Replication: Successful sampling achieved in at least three of the four replicate treatments (minimum n = 3).

## Treatments
- Control: No urine application.
- Artificial sheep urine (ArtUrine): Applied in discrete patches (each patch: 200 mL artificial urine over 100 cm2 soil surface; N application rate of 1120 kg N ha-1).
- Nitrate and glucose (RealUrine reference): Nitrate and glucose applied (106 kg N ha-1; 213 kg C ha-1) in a 40 cm x 40 cm square within plots.
- Application date: 25/10/17.

## Sampling, storage, and handling
- Sample collection and storage: Soil solutions collected and stored frozen at -20 °C until analysis.
- Timekeeping: Date field records indicate the date of soil sample collection; Day indicates days after treatment application.

## Laboratory analysis
- Ammonium (NH4+): Measured by the method of Mulvaney (1996).
- Nitrate (NO3-): Measured by the method of Miranda et al. (2001).
- Additional measurements: Dissolved organic carbon (DOC) and total dissolved nitrogen (TN) using a Multi N/C 2100S analyzer (AnalytikJena, Jena, Germany).
- Calibration/quality: All solutions analyzed against certified reference standard solutions.

## Data structure and fields
- Date: Date of soil sample collection (dd/mm/yyyy).
- Day: Days after treatment application.
- Treatment: Accounted as 'Control', 'ArtUrine', or 'RealUrine' (note: 'RealUrine' is used for the urine treatments; 'ArtUrine' for artificial urine).
- Chamber: Plot and chamber identifier.
- Nitrate: NO3--N concentration in mg NO3--N L-1.
- Ammonium: NH4+-N concentration in mg NH4+-N L-1.
- DOC: Dissolved organic carbon in mg C L-1.
- TN: Total dissolved nitrogen in mg N L-1.

## Data quality, replication, and limitations
- Replication: Minimum of three replicates per treatment when sampling was successful.
- Data completeness: Reflection of successful sample collection in at least three out of four replicates; potential gaps if a replicate was not collected.
- Considerations for GIS use: Spatially limited to the plotted chambers and treatment patches; time-series integration possible via the Day and Date fields; geographic context tied to exact plot locations within the study site.

## Usage notes and attribution
- Authors must be acknowledged if data are reused or reproduced.

## References
- Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. pp. 1123-1184.
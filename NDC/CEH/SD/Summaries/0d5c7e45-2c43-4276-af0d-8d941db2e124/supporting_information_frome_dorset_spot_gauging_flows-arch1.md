# River Frome Dorset spot gauging flows

- A dataset of spot gauged river flows (m3 s-1) at multiple sites along the River Frome, Dorset, UK, collected during 2022.
- In total, 19 river channels were spot gauged across 11 river cross-sections along the lower River Frome reach between Dorchester and East Stoke EA gauging stations; some cross-sections required multiple channels due to the braided river.
- Monitoring sites include major tributaries: South Winterbourne, Tadnoll Brook, and the River Win; cross-section locations are roughly 3 km apart, chosen mainly by accessibility and suitability for flow measurements.
- NGR coordinates for all monitoring sites are provided to enable mapping; some sites are on private land with access permissions required.
- Measurements were taken on multiple flow accretion survey days between 12 April 2022 and 5 November 2022, with surveying conducted upstream to downstream each day.

## Location, reach and timing

- Study area spans the lower River Frome, from the Dorchester gauging station to East Stoke.
- River geometry includes braided sections necessitating measurement of multiple channels per cross-section to obtain total discharge.
- Flow accretion survey days are listed in the dataset; not all sites could be monitored on every day due to time or weather constraints.

## Measurement methods

- The river channel was divided into at least 10 evenly spaced transects (5–10 for very small streams). Depth and flow velocity were recorded at each transect.
- Flow velocity measured at 40% depth above the riverbed using Valeport current meters (models 001 and 002); for small streams, the 5–10 transect approach was used.
- Cross-sectional area per transect = width × average depth of the two adjacent transects; discharge per transect = cross-sectional area × average velocity of the two adjacent transects; total discharge is the sum across transects.
- Calibration/processing involved converting impeller revolutions to velocity via a bespoke spreadsheet, with velocity depending on the impeller model (BMF001 or BMF002).
- Only one recording per site per survey day was made (no replicates) due to time constraints.
- Some sites required multiple channels to represent a single cross-section because of braided channels; unit measurements are in m3 s-1.

## Data structure

- The dataset is contained in a single CSV file entitled River_Frome_Dorset_spot_gauging_flows.
- Seven columns: Site, Description, NGR, Date, Start_time, Flow, Impeller.
  - Site: monitoring site name.
  - Description: brief site location description (e.g., near footbridge).
  - NGR: British National Grid Reference for the site.
  - Date: measurement date.
  - Start_time: time the measurement started.
  - Flow: total discharge for that stream channel in m3 s-1.
  - Impeller: flow impeller used (BMF001 or BMF002).

## Quality, caveats and completeness

- Most flows were very low during the monitoring period due to one of the hottest and driest summers on record.
- Pallington Lakes flow on 09/05/22 is suspected to be underestimated; BMF001 impeller may have under-recorded shallow flows compared with BMF002.
- Environment Agency gauging station data are available for the same dates (Louds Mill, Stinsford, East Stoke) for reference upstream/downstream flows.
- Data quality control notes: formal QA details are not provided (Quality Control section lists N/A).
- Completeness: on most survey days, not all sites could be monitored; several dates are missing for certain sites.

## Provenance, accessibility and use

- Collected by Thomas Homan (PhD candidate, University of Bath) with supervision from Prof. Jan Hofman; data compiled and checked by Thomas.
- Equipment loaned by Wessex Water Ltd.
- Data intended to support hydrodynamic modeling of nutrient fate and transport in the River Frome; suitable for analyses of flow accretion along the reach and cross-section hydrology.
- Where relevant, users can cross-check against EA gauging stations to contextualize upstream/downstream flows.

## Miscellaneous notes

- The exact measurement locations, cross-sections, and site NGRs are documented (including private land considerations and specific site descriptions such as LMbypass and others).
- The dataset provides the necessary metadata to plot sites (via NGR) and to reproduce calculations if velocity-to-flow conversions or cross-sectional computations are needed.
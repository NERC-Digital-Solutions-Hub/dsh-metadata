# Overview of data

- Purpose and scope
  - Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, focusing on the role of lateral exchange in the seaward flux of carbon, nitrogen, and phosphorus.
  - Accompanies a single dataset file: O2fluxes_Avon.CSV.
  - Methods combine benthic O2 flux measurements (via aquatic eddy covariance) and water-column O2 flux measurements (via bottle incubations).

- Field campaigns and sites
  - Four field campaigns: spring 2013, summer 2013, autumn 2013, winter 2014.
  - Regions: six tributaries of the Hampshire River Avon catchment.
  - Site codes and approximate locations:
    - CE1 — River Ebble (51.027499 N, -1.9217089 E)
    - GA2 — River Avon (51.318289, -1.8600020)
    - GN1 — River Nadder (51.043849, -2.1118158)
    - CW2 — River Wylye (51.142475, -2.2033140)
    - AS1 (aka AP) — tributary of River Sem (51.055413, -2.1568407)
    - AS2 (aka AS) — River Sem (51.045826, -2.1104425)
  - Note on data quality and availability:
    - CE1 was not sampled during the winter campaign due to extensive flooding.
    - Winter and autumn data at GA2 did not meet quality requirements and were omitted.
    - Missing data due to technical issues or sampling contamination are marked as not determined (n.d.).

- Data collection methods
  - Benthic O2 fluxes (benthic metabolism) measured with aquatic eddy covariance (AEC); processing follows Attard et al. (2014) and Rovelli et al. (2015) protocols; foundational methodology described by Berg et al. (2003).
  - Water-column O2 fluxes measured by incubating water samples (100 mL bottles) for 24 hours with optical O2 sensors monitoring concentration.

- Dataset structure and key variables
  - Campaign: season of data collection.
  - Site: sampling location within the campaign.
  - Depth: average stream depth (m) from flow-transect data.
  - Day flux (b): daytime benthic flux (mmol/m2/h) with SE; number of data points shown in parentheses.
  - Night flux (b): nighttime benthic flux (mmol/m2/h) with SE.
  - Total PAR (b): daily-integrated PAR at the streambed (mol/m2/d).
  - Daylight (b): daytime duration (hours) at the streambed.
  - Day flux (w): daytime water-column flux (µmol/L/h) with data count; values below detection listed as <0.1 µmol/L/h.
  - Night flux (w): nighttime water-column flux (µmol/L/h).
  - Total PAR (w): daily-integrated PAR in the water column near the surface (mol/m2/d).
  - Daylight (w): daytime duration (hours) near the water surface.
  - Data quality flags: n.d. marks missing data due to technical issues or contamination.

- Usage context and references
  - Data underpin analyses of benthic and water-column oxygen dynamics across seasons and sites within the Hampshire Avon catchment.
  - Related methodological and interpretive references include:
    - Attard et al. 2014; Berg et al. 2003; Rovelli et al. 2015; Rovelli et al. 2016.
    - Data described in Rovelli et al. (submitted) and related Limnology & Oceanography submissions.
  - Access and provenance: Data are archived and described through the NERC Environmental Information Data Centre; linked publications provide detailed methodology and interpretation.
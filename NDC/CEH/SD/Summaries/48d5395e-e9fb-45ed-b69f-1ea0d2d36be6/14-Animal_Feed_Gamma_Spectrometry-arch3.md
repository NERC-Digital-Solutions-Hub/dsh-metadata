# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Purpose and scope
- Provides metadata definitions and field meanings for a dataset measuring radionuclide activity in animal feed on a dry-mass basis.
- Intended to support monitoring, evaluation of environmental health policies, and informing future decisions.
- Designed to aid data governance, quality assurance, and clear reporting through outputs such as reports, charts, or dashboards.

## Data fields and definitions
- Animal: General type of animal; Units and Notes not applicable.
- Location: Name of the sampling location; Units and Notes not applicable.
- Feeding: Description of the feeding regime; Units and Notes not applicable.
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 in the total diet on a dry mass basis; Units = Bq per kg dry mass; Notes: in equilibrium with Pb-214 and Bi-214; where blank, concentration was below the detection limit.
- Unc_Ra-226_Bq/kg_dm: Uncertainty (quadratic propagation) of Ra-226 concentration; Units = Bq per kg dry mass; Notes: in equilibrium with Pb-214 and Bi-214.
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226; Units = Bq per kg dry mass; Notes: in equilibrium with Pb-214 and Bi-214; where blank, concentration was above the detection limit.
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137; Units = Bq per kg dry mass; Notes: where blank, concentration was below the detection limit.
- Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration; Units = Bq per kg dry mass; Notes: where blank, concentration was below the detection limit.
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137; Units = Bq per kg dry mass; Notes: where blank, concentration was above the detection limit.
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228; Units = Bq per kg dry mass; Notes: in equilibrium with Ac-228; where blank, concentration was below the detection limit.
- Unc_Ra-228_Bq/kg_dm: Uncertainty of Ra-228 concentration; Units = Bq per kg dry mass; Notes: in equilibrium with Ac-228.
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228; Units = Bq per kg dry mass; Notes: in equilibrium with Ac-228; where blank, concentration was above the detection limit.
- K-40_Bq/kg_dm: Activity concentration of K-40; Units = Bq per kg dry mass; Notes: below detection limit when blank.
- Unc_K-40_Bq/kg_dm: Uncertainty of K-40 concentration; Units = Bq per kg dry mass; Notes: below detection limit when blank.
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40; Units = Bq per kg dry mass; Notes: where blank, concentration was above the detection limit.

## Measurement interpretation and data quality
- All radionuclide measurements are expressed as activity concentrations in the total diet on a dry-mass basis (Bq/kg_dm).
- Uncertainties are provided as quadratic propagations where available.
- Detection limits accompany each radionuclide to indicate non-detect values; blanks in activity fields mean concentrations were below detection limits; blanks in detection-limit fields imply concentrations were above the detection limit.
- Equilibrium relationships are noted (e.g., Ra-226 with Pb-214 and Bi-214; Ra-228 with Ac-228), which can affect interpretation and comparability across datasets.

## Data governance, metadata and sharing considerations
- Emphasizes the need for complete, well-documented metadata to enable verification and reuse.
- Public sharing of underlying data is common but can be a barrier due to data sensitivity or governance rules.
- Data quality steps include data provenance, cleaning, transformation, and clear presentation of findings (reports, charts, dashboards).
- Encourages identifying data sources, addressing gaps by commissioning new data when needed, and establishing data management standards at the source.
- Highlights potential barriers relevant to monitoring frameworks: data gaps, data access issues, organisational silos, metadata inadequacy, and the need for robust data governance.

## Implications for monitoring frameworks
- The dataset supports environmental health monitoring and policy evaluation by providing standardized measurements of radionuclide contamination in animal feed.
- Clear unit definition (Bq/kg_dm) and equilibrium notes facilitate cross-dataset comparability and transparent reporting.
- The presence of detection limits and handling of non-detect values informs interpretation and risk assessment.
- To maximize utility in dashboards and policy reviews, ensure comprehensive metadata, open data where possible, and consistent data governance practices to overcome barriers such as data silos and incomplete metadata.
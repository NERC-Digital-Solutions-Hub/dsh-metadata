### Rate of emergency admission to hospital (Z-Score)

**Description:**
This field (referred to as `ZEmergencyHospitalAdmiss` in the spatial dataset) represents the standardized Z-score for the rate of emergency hospital admissions within a given Lower Super Output Area (LSOA). It measures how the local rate of acute morbidity in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is one of the key supporting indicators within the "Health" domain used to calculate a community's overall "Sensitivity" to climate hazards like floods and heatwaves. A higher rate of emergency admissions indicates poorer underlying health in the local population. People in poor health are more socially vulnerable to the impacts of extreme weather because the experience can exacerbate pre-existing medical conditions, either as an immediate one-off shock or by accelerating an adverse health trajectory. Additionally, extreme weather can restrict access to vital medicines and home-based healthcare systems, and it carries significant mental health stresses. 

**Interpretation:**
Standardizing this metric as a Z-score allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of emergency hospital admissions than the national average, indicating higher relative vulnerability.
*   **Values around 0** indicate that the rate is approximately average for England.
*   **Negative values** signify a lower rate of emergency admissions than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into the following standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD). Specifically, it utilizes the "Acute Morbidity" indicator from the Health Deprivation and Disability Domain, which is sourced from the Health and Social Care Information Centre. It carries a 0.143 weighting within the broader Health domain.
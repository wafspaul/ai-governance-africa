# Data Sources

Raw data files are not committed to this repository (see `.gitignore`). Download them directly from the sources below and place them in the indicated folders.

---

## ILO Data — `data_raw/ilo/`

All files downloaded from [ILOSTAT](https://ilostat.ilo.org/data/) — Kenya, latest available year (2022 for most indicators; 2019 for ISIC-2 informality breakdown).

| File (in `data_raw/ilo/`) | ILOSTAT Indicator | Description |
|---|---|---|
| `ILO_Data.csv` | `EMP_TEMP_SEX_AGE_EDU_NB_A` | Employment by sex, age, education — headline file used throughout notebook |
| `employment/emp_by_age_education.csv` | `EMP_TEMP_SEX_AGE_EDU_NB_A` | Employment by age and education level |
| `employment/emp_by_activity_education.csv` | `EMP_TEMP_SEX_ECO_EDU_NB_A` | Employment by economic activity and education |
| `employment/emp_by_occupation_education.csv` | `EMP_TEMP_SEX_OCU_EDU_NB_A` | Employment by occupation and education |
| `employment/emp_by_activity_isic2.csv` | `EMP_TEMP_SEX_EC2_NB_A` | Employment by ISIC-2 sub-sector |
| `employment/emp_by_occupation_isco2.csv` | `EMP_TEMP_SEX_OC2_NB_A` | Employment by ISCO-2 occupation |
| `employment/emp_by_occupation_isco2_19icls.csv` | `EMP_5EMP_SEX_OC2_NB_A` | Employment by occupation (19th ICLS definition) |
| `employment/emp_by_activity_modelled.csv` | `EMP_2EMP_SEX_ECO_NB_A` | Employment by activity (modelled estimates) |
| `employment/emp_to_population_ratio_by_age.csv` | `EMP_5WAP_SEX_AGE_RT_A` | Employment-to-population ratio by age |
| `informal/informal_emp_by_education.csv` | `EMP_NIFL_SEX_EDU_NB_A` | Informal employment by education level |
| `informal/informal_emp_by_broad_sector.csv` | `EMP_NIFL_SEX_ECO_NB_A` | Informal employment by broad sector |
| `informal/informal_emp_by_activity_isic2.csv` | `EMP_NIFL_SEX_EC2_NB_A` | Informal employment by ISIC-2 sub-sector |
| `informal/informal_emp_by_age_count.csv` | `EMP_NIFL_SEX_AGE_NB_A` | Informal employment count by age |
| `informal/informal_emp_rate_by_age.csv` | `EMP_NIFL_SEX_AGE_RT_A` | Informal employment rate by age |
| `informal/outside_formal_sector_rate_by_age.csv` | `EMP_PIFL_SEX_AGE_RT_A` | Share outside formal sector by age |
| `earnings/avg_monthly_earnings_by_education.csv` | `EAR_EMTA_SEX_EDU_NB_A` | Average monthly earnings by education |
| `earnings/avg_monthly_earnings_by_activity.csv` | `EAR_EMTA_SEX_ECO_NB_A` | Average monthly earnings by economic activity |
| `earnings/median_monthly_earnings_by_education.csv` | `EAR_EMTM_SEX_EDU_NB_A` | Median monthly earnings by education |
| `underemployment/underemployment_rate_by_age.csv` | `TRU_DEMP_SEX_AGE_RT_A` | Time-related underemployment rate by age |
| `underemployment/underemployment_rate_by_education.csv` | `TRU_DEMP_SEX_EDU_RT_A` | Time-related underemployment rate by education |
| `youth/neet_rate_by_sex.csv` | `EIP_NEET_SEX_RT_A` | NEET rate by sex |
| `youth/unemployment_rate_by_age_education.csv` | `UNE_3EAP_SEX_AGE_EDU_RT_A` | Unemployment rate by age and education |
| `labour_force/lfpr_by_age_modelled.csv` | `EAP_2WAP_SEX_AGE_RT_A` | Labour force participation rate by age (modelled) |
| `sdg/sdg_1_1_1_working_poverty.csv` | `SDG_0111_SEX_AGE_RT_A` | SDG 1.1.1 — Working poverty rate |
| `sdg/sdg_8_3_1_informal_employment.csv` | `SDG_0831_SEX_ECO_RT_A` | SDG 8.3.1 — Informal employment share |
| `sdg/sdg_8_3_1_informal_employment_19icls.csv` | `SDG_B831_SEX_ECO_RT_A` | SDG 8.3.1 — Informal employment (19th ICLS) |
| `sdg/sdg_8_6_1_neet.csv` | `SDG_0861_SEX_RT_A` | SDG 8.6.1 — NEET rate |

**Download steps:**
1. Go to [https://ilostat.ilo.org/data/](https://ilostat.ilo.org/data/)
2. Select indicator → filter by Country: Kenya → download CSV
3. Place in the subfolder matching the indicator category above

---

## World Bank Data — `data_raw/world_bank/`

All files downloaded from [World Bank WDI](https://data.worldbank.org/). Load pattern in notebooks: `pd.read_csv(path, skiprows=4)`, then extract the Kenya row and transpose year columns as a time series.

| Subfolder | WDI Indicator Code | Description |
|---|---|---|
| `unemployment/youth_unemployment_female_ilo/` | `SL.UEM.1524.FE.ZS` | Youth unemployment rate — female (ILO modelled) |
| `unemployment/youth_unemployment_male_ilo/` | `SL.UEM.1524.MA.ZS` | Youth unemployment rate — male (ILO modelled) |
| `unemployment/youth_unemployment_total_national/` | `SL.UEM.1524.NE.ZS` | Youth unemployment — national estimate |
| `unemployment/unemployment_total_ilo_modeled/` | `SL.UEM.TOTL.ZS` | Total unemployment rate (ILO modelled) |
| `unemployment/unemployment_total_national/` | `SL.UEM.TOTL.NE.ZS` | Total unemployment — national estimate |
| `unemployment/unemployment_female_national/` | `SL.UEM.TOTL.FE.NE.ZS` | Female unemployment — national |
| `unemployment/unemployment_male_national/` | `SL.UEM.TOTL.MA.NE.ZS` | Male unemployment — national |
| `unemployment/unemployment_advanced_education/` | `SL.UEM.ADVN.ZS` | Unemployment — advanced education |
| `unemployment/unemployment_basic_education/` | `SL.UEM.BASC.ZS` | Unemployment — basic education |
| `labour_force/female_labour_force_participation/` | `SL.TLF.TOTL.FE.ZS` | Female share of labour force |
| `labour_force/female_labour_force_basic_education/` | `SL.TLF.BASC.FE.ZS` | Female labour force — basic education |
| `education/secondary_enrolment_gross/` | `SE.SEC.ENRR` | Secondary school gross enrolment ratio |
| `education/secondary_enrolment_net/` | `SE.SEC.NENR` | Secondary school net enrolment ratio |
| `education/tertiary_enrolment_gross/` | `SE.TER.ENRR` | Tertiary gross enrolment ratio |
| `economic/gross_domestic_investment/` | `NE.GDI.TOTL.ZS` | Gross domestic investment (% of GDP) |

**Download steps:**
1. Go to [https://data.worldbank.org/indicator/](https://data.worldbank.org/indicator/) + the code above
2. Filter to Kenya → download CSV (includes metadata files — keep them)
3. Place all three files (data + two metadata CSVs) in the subfolder above

---

*Last updated: April 2026*

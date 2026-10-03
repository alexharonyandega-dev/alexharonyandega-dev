# Hi, I'm Alex

**16-year-old Kenyan student building Kenya Climate Data Lab** — an open-source drought and vegetation stress monitor for all 47 Kenyan counties.

[![Substack](https://img.shields.io/badge/Substack-Kenya%20Climate%20Lab-FF6719?style=for-the-badge&logo=substack&logoColor=white)](https://kenyaclimatelab.substack.com)
[![X](https://img.shields.io/badge/X-@KenyaClimateLab-000000?style=for-the-badge&logo=x)](https://x.com/KenyaClimateLab)
[![Email](https://img.shields.io/badge/Email-alexharonyandega@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alexharonyandega@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Kenya%20Climate%20Data%20Lab-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alexharonyandega-dev/kenya-climate-data-lab)

---

## What I'm building

Kenya Climate Data Lab is a 72-week open-source project building a **weekly county-level drought and vegetation stress monitor** for all 47 counties in Kenya.

It combines CHIRPS satellite rainfall and Sentinel-2 vegetation health (NDVI) into a composite stress index. The tool detects droughts **without calibration** by comparing each county-month to its own historical average.

**The gap it fills:** Existing tools that update often don't give county-level numbers. The tool that does — KNBS — publishes once a year, post-harvest. By the time a county officer knows there's a drought, the crop is already lost.

## What I found

**1. Drought ≠ crop damage.**

In 2022, 31 Kenyan counties experienced severe drought. Only **8** experienced severe drought *while maize was actively growing* — Bomet, Busia, Homa Bay, Kericho, Kilifi, Laikipia, Nandi, Nyamira. Those 8 are where the drought actually damaged maize yield. Notably, Kenya's largest maize producers aren't on the list — they had already harvested.

**2. Soil moisture leads vegetation by 1 month.**

`swvl1_mean_anomaly` at time *t−1* predicts `ndvi_anomaly` at time *t* with **r = 0.461** (95% CI [0.436, 0.485], p = 6e-223). Entirely temporal — survives county demeaning without shrinkage.

**3. The tool covers a drought regime NDMA does not classify.**

Kenya's National Drought Management Authority tracks pastoral drought in 23 ASAL counties. In October 2022, NDMA flagged 11 counties as Alarm — all in the arid north. The monitor flagged a completely different set of 10 counties — the highland maize belt and the coast. Zero overlap.

CHIRPS verification: monitor counties averaged October 2022 rainfall z-score of −1.14; NDMA counties averaged −0.71. Both groups were in drought. The two systems track different things — NDMA by cumulative pastoral impact, the monitor by current-month rainfall and vegetation anomaly for all 47 counties.

The tool is complementary to NDMA, not competing. Cross-checked against NDMA, CCRP, TAMSAT, and KMD.

**4. The tool is a drought monitor, not a yield predictor.**

I tried to validate the stress index against KNBS county yield data. Every meaningful test came back null, wrong-signed, or untestable. One county — Kakamega — had the mildest 2022 stress and the worst yield crash (−42.5%). The cause was a fall armyworm outbreak, confirmed in the National Agriculture Production Report 2025, page 31. The tool caught the drought. It cannot see the pest.

Documented publicly: [I Tried to Validate My Tool. It Failed.](https://kenyaclimatelab.substack.com/p/i-tried-to-validate-my-tool-it-failed)

All findings are hardened: 28 weight combinations tested, within-county verification, 1,000-resample bootstrap, CHIRPS rainfall verification.

## Current status

- **Phase:** Foundation — Week 5 of 72
- **Master table:** 4,512 rows × 27 columns (47 counties × 96 months)
- **Weekly product:** 19,599 rows
- **Validation:** 2022 Horn of Africa drought detected without calibration
- **Null result:** stress index does not predict county-level yield loss (documented)
- **Next:** Draft the preprint abstract and methods section

## Public writing

- [I Tried to Validate My Tool. It Failed.](https://kenyaclimatelab.substack.com/p/i-tried-to-validate-my-tool-it-failed) — the null result
- [An open letter to Kenya's county agriculture officers](https://kenyaclimatelab.substack.com/p/an-open-letter-to-kenyas-county-agriculture) — the ask
- [Kenya Climate Data Lab on Substack](https://kenyaclimatelab.substack.com)

## Tech I use

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=flat-square)
![xarray](https://img.shields.io/badge/xarray-2024.1-3b82f6?style=flat-square)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-4285F4?style=flat-square&logo=google-earth&logoColor=white)

## Get in touch

The best way to reach me is by replying to any post on the [Substack](https://kenyaclimatelab.substack.com). I read every message.

Or email me: **alexharonyandega@gmail.com**

## What I need

I'm looking for:

- **County agriculture officers** — 20 minutes to tell me what signal would make you act
- **County-level maize yield records** — any format, any county
- **Developers** — the repo is MIT licensed, the decisions log tells you why every choice was made
- **Anyone with a platform** — forward this to someone who needs it

**The code is open, the door is open, and the inbox is open.**

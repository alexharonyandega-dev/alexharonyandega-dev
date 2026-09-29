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

Both findings are hardened: 28 weight combinations tested, within-county verification, 1,000-resample bootstrap.

## Current status

- **Phase:** Foundation — Week 4 of 72
- **Master table:** 4,512 rows × 27 columns (47 counties × 96 months)
- **Weekly product:** 19,599 rows
- **Validation:** 2022 Horn of Africa drought detected without calibration
- **Next:** Formal validation against KNBS county yield data

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

# How fast is the Bay of Bengal warming?

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ratulripon/bay-of-bengal-sst/blob/main/bay_of_bengal_sst.ipynb)

An analysis of four decades of satellite-based sea surface temperature (SST) in the Bay of Bengal, using NOAA's Optimum Interpolation SST dataset. The notebook answers three questions:

1. **How fast** has the basin-average SST risen since 1982, and is the trend statistically significant?
2. **When in the year** is the warming strongest: winter, pre-monsoon, monsoon or post-monsoon?
3. **Where** in the Bay is it warming fastest?

**Results:** [ratulripon.github.io/projects/bay-of-bengal-sst](https://ratulripon.github.io/projects/bay-of-bengal-sst/)

## Methods in brief

| Step | Method |
|---|---|
| Data | NOAA OI SST V2 High Resolution, monthly means, 0.25° grid |
| Study area | 5–23°N, 80–95°E (land cells excluded) |
| Basin average | Area-weighted by cos(latitude) |
| Anomalies | Departures from the 1991–2020 monthly climatology |
| Trend | Sen's slope on annual means, Mann–Kendall significance test, OLS cross-check |
| Seasons | Winter (Dec–Feb), pre-monsoon (Mar–May), monsoon (Jun–Sep), post-monsoon (Oct–Nov) |
| Spatial trend | Per-cell least-squares trend of annual means, t-test on the slope |

## Run it

**In Google Colab (easiest):** click the badge above and choose *Runtime → Run all*. The notebook downloads only the Bay of Bengal subset from NOAA (a few MB), so it takes a few minutes.

**Locally:**

```bash
pip install -r requirements.txt
jupyter notebook bay_of_bengal_sst.ipynb
```

## Outputs

- `output/figures/`: full-resolution PNG figures
- `output/website/bay-of-bengal-sst/`: a ready-to-upload results page (HTML, WebP figures, `results.json`, monthly data as CSV)

The results page is built from `page_template.html`, so every number on it comes from the notebook run.

## Data credit

NOAA OI SST V2 High Resolution Dataset data provided by the NOAA PSL, Boulder, Colorado, USA, from their website at https://psl.noaa.gov.

Huang, B., Liu, C., Banzon, V., et al. (2021). Improvements of the Daily Optimum Interpolation Sea Surface Temperature (DOISST) Version 2.1. *Journal of Climate*, 34, 2923–2939.

## Author

MD Ratul Hasan Ripon, BSc (Hons) Oceanography, Shahjalal University of Science and Technology
[Portfolio](https://ratulripon.github.io/) · [LinkedIn](https://www.linkedin.com/in/ratul-ripon/)

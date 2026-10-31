# Bike Share Analysis Dashboard (Power BI)

An interactive Power BI dashboard analysing bike-rental demand, revenue and profit across 2021 and 2022, built as part of **Boycode Africa Cohort 5.0 Data Analysis Class**.

![Dashboard – all years](images/Bike_dashboard_all_years.png)

## Key figures (both years)

| Metric | Value |
|---|---|
| Total riders | ~3.29M |
| Revenue | ~$15M |
| Profit | ~$10.45M |
| Profit margin | 68.80% |
| Rider mix | 81.17% registered / 18.83% casual |

2021 only: ~1.24M riders, ~$5M revenue, ~$3.42M profit, 68.92% margin.

![Dashboard – 2021](images/Bike_dashboard_2021.png)

2022 only: ~2M riders, ~$10M revenue, ~$7.03M profit, 68.74% margin.

![Dashboard – 2022](images/Bike_dashboard_2022.png)

## What the dashboard shows

- **Year slicer** (2021 / 2022) that filters every visual
- **KPI cards:** riders, revenue, profit, profit margin
- **KPI over time:** monthly riders (columns) with average revenue and average profit (lines)
- **Hour × weekday matrix:** revenue by hour of day (rows) and weekday (columns), showing the late-afternoon peak
- **Seasonal revenue:** average revenue by season
- **Rider demographics:** registered vs. casual riders

## Repository structure

```
├── report/Bike_share_dashboard.pbix   # Power BI report (data imported)
├── images/                            # Dashboard screenshots
├── data/README.md                     # Where to get the source CSVs
└── README.md
```

## How to use

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Open `report/Bike_Share_Dashboard.pbix`.
3. Use the 2021 / 2022 buttons to filter.

## Data model (fields used)

`Query` table: `dteday`, `yr`, `season`, `weekday`, `hr`, `rider_type`, `riders`, `Revenue`, `Profit`, plus a `Profit Margin` measure and a date hierarchy (`Year`, `Month`).

## Verification

Figures were recomputed from the source CSVs (revenue = `riders × price`; profit = `riders × (price − COGS)`):

| | Riders | Revenue | Profit | Margin | Registered |
|---|---|---|---|---|---|
| 2021 | 1,243,103 | $4.96M | $3.42M | 68.92% | 80.11% |
| 2022 | 2,049,576 | $10.23M | $7.03M | 68.74% | 81.81% |
| Both | 3,292,679 | $15.19M | $10.45M | 68.80% | 81.17% |

The busiest hours are 17:00 and 18:00 (5–6 PM).


## Data source & attribution

The datasets come from [Gaelim/YT_bike_share](https://github.com/Gaelim/YT_bike_share). I did not create the data. The dashboard design, data modelling and analysis in this repository are my own work.
That source repository does not state a license, so the data is linked rather than copied here.

## Author

Chibuokem Nathan Success Godwin · [LinkedIn](linkedin.com/in/chibuokem-godwin-082b271b3) · [GitHub](https://github.com/hibuokem)

# India-Stocks-2071-2100-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2071 to 2100)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2071-2100-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2071 to 2100)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2071 | `SAB` | SAB Industries Limited | `SAB.NS` |
| 2072 | `SADBHAV` | Sadbhav Engineering Limited | `SADBHAV.NS` |
| 2073 | `SADBHIN` | Sadbhav Infrastructure Project Limited | `SADBHIN.NS` |
| 2074 | `SADHNANIQ` | Sadhana Nitrochem Limited | `SADHNANIQ.NS` |
| 2075 | `SAFARI` | Safari Industries (India) Limited | `SAFARI.NS` |
| 2076 | `SAGARDEEP` | Sagardeep Alloys Limited | `SAGARDEEP.NS` |
| 2077 | `SAGCEM` | Sagar Cements Limited | `SAGCEM.NS` |
| 2078 | `SAHLIBHFI` | Shalibhadra Finance Limited | `SAHLIBHFI.NS` |
| 2079 | `SAHYADRI` | Sahyadri Industries Limited | `SAHYADRI.NS` |
| 2080 | `SAICAPI` | Sai Capital Limited | `SAICAPI.NS` |
| 2081 | `SAIPARENT` | Sai Parenterals Limited | `SAIPARENT.NS` |
| 2082 | `SAKAR` | Sakar Healthcare Limited | `SAKAR.NS` |
| 2083 | `SAKHTISUG` | Sakthi Sugars Limited | `SAKHTISUG.NS` |
| 2084 | `SAKSOFT` | Saksoft Limited | `SAKSOFT.NS` |
| 2085 | `SAKUMA` | Sakuma Exports Limited | `SAKUMA.NS` |
| 2086 | `SALASAR` | Salasar Techno Engineering Limited | `SALASAR.NS` |
| 2087 | `SALONA` | Salona Cotspin Limited | `SALONA.NS` |
| 2088 | `SALSTEEL` | S.A.L. Steel Limited | `SALSTEEL.NS` |
| 2089 | `SALZERELEC` | Salzer Electronics Limited | `SALZERELEC.NS` |
| 2090 | `SAMBANDAM` | Sambandam Spinning Mills Limited | `SAMBANDAM.NS` |
| 2091 | `SAMBHAAV` | Sambhaav Media Limited | `SAMBHAAV.NS` |
| 2092 | `SAMBHV` | Sambhv Steel Tubes Limited | `SAMBHV.NS` |
| 2093 | `SAMHI` | Samhi Hotels Limited | `SAMHI.NS` |
| 2094 | `SAMPANN` | Sampann Utpadan India Limited | `SAMPANN.NS` |
| 2095 | `SANATHAN` | Sanathan Textiles Limited | `SANATHAN.NS` |
| 2096 | `SANDESH` | The Sandesh Limited | `SANDESH.NS` |
| 2097 | `SANDHAR` | Sandhar Technologies Limited | `SANDHAR.NS` |
| 2098 | `SANDUMA` | Sandur Manganese & Iron Ores Limited | `SANDUMA.NS` |
| 2099 | `SANGAMIND` | Sangam (India) Limited | `SANGAMIND.NS` |
| 2100 | `SANGHVIMOV` | Sanghvi Movers Limited | `SANGHVIMOV.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SAB 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2071-2100-Historical-Data/main/SAB/1m/2026/10/SAB_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```

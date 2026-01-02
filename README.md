# AdventureWorks Forsaljningsanalys

Jupyter Notebook-projekt for analys av AdventureWorks-databasen med Python och SQL Server.

## Innehall

- **7 visualiseringar** som besvarar affarsfragor
- **Kundvarde-analys** med RFM-segmentering
- **Pivot tables** for kundsegmentering
- **Sammanfattning** med rekommendationer

## Krav

### Python-bibliotek
```bash
pip install pandas matplotlib seaborn sqlalchemy pyodbc numpy
```

### Databas
- Microsoft SQL Server med AdventureWorks2022-databasen
- ODBC Driver 17 eller 18 for SQL Server

## Installation

1. Klona repot:
```bash
git clone <repo-url>
cd SQL
```

2. Installera dependencies:
```bash
pip install -r requirements.txt
```

3. Konfigurera databasanslutning i notebooken (Setup-cellen)

## Databasanslutning

Notebooken stodjer tre anslutningsmetoder:

### Docker (Linux/Mac)
```python
server = 'localhost,1433'
driver = 'ODBC Driver 18 for SQL Server'
```

### SSMS (Windows)
```python
server = 'localhost'
driver = 'ODBC Driver 17 for SQL Server'
```

### SQL Server med losenord
```python
server = 'localhost'
username = 'sa'
password = 'ditt_losenord'
```

## Visualiseringar

| # | Analys | Diagramtyp |
|---|--------|------------|
| 1 | Antal produkter per kategori | Stapeldiagram (bar) |
| 2 | Forsaljning per produktkategori | Horisontellt stapeldiagram (barh) |
| 3 | Forsaljningstrend per manad | Linjediagram (line) |
| 4 | Forsaljning och ordrar per ar | Grupperat stapeldiagram |
| 5 | Top 10 produkter | Horisontellt stapeldiagram (barh) |
| 6 | Forsaljning och kunder per region | Grupperat stapeldiagram |
| 7 | Ordervarde per region och kundtyp | Grupperat stapeldiagram |

## Kundvarde-analys

- Top 20 kunder efter inkopsvarde
- RFM-segmentering (Recency, Frequency, Monetary)
- Kundsegment-pivot (Store vs Individual)
- Kundlivscykel per kohort

## Anvandning

1. Oppna `AdventureWorks_Forsaljningsanalys.ipynb` i Jupyter Notebook/Lab
2. Konfigurera databasanslutningen i Setup-cellen
3. Kor alla celler (Run All)

## Tabeller som anvands

**Production-schema:**
- ProductCategory
- ProductSubcategory
- Product

**Sales-schema:**
- SalesOrderHeader
- SalesOrderDetail
- Customer
- SalesTerritory
- Store

## Licens

Detta projekt ar skapat for utbildningssyfte.

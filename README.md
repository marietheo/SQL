# AdventureWorks - Försäljningsanalys

Analys av försäljningsdata från AdventureWorks-databasen med fokus på:
- Produktkategorier och omsättning
- Försäljningstrender över tid
- Regional försäljning och kundtyper
- Kundsegmentering och churn-analys

## Miljö
- **Python:** 3.13.7
- **Databas:** SQL Server Express (AdventureWorks2025)
- **Paket:** Pandas, NumPy, Matplotlib, Seaborn, SQLAlchemy, PyODBC

## Kom igång
```bash
# Klona projektet
git clone https://github.com/marietheo/SQL.git
cd SQL

# Skapa och aktivera virtuell miljö
python -m venv .venv

# Windows
.venv\Scripts\activate

# Mac/Linux
source .venv/bin/activate

# Installera beroenden
pip install -r requirements.txt
```

## Databasanslutning
Uppdatera anslutningsuppgifterna i notebook-filen vid behov:
```python
server = 'localhost\\SQLEXPRESS'
database = 'AdventureWorks2025'
```

## Sammanfattning

Analysen visar att merparten av omsättningen är koncentrerad till ett fåtal B2B-kunder, vilket utgör en affärsrisk. 

**Rekommendationer:**
- Identifiera whitespace för tillväxt i befintlig kundbas
- Prioritera uppföljning av "At Risk"-kunder innan de churnar
- Säkerställa pipeline med högvärdiga prospects
- Utreda orsaken till den kraftiga omsättningsdippen
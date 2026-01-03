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

# Sammanfattning

## Huvudsakliga fynd

- **Bikes dominerar omsättningen** – 94,7M USD (ca 85% av total försäljning), trots att Components har flest produkter
- **B2B står för merparten av kundvärdet** – Top 20-listan består enbart av företagskunder
- **Kraftig omsättningsdipp** – försäljningen störtdök på kort tid, orsaken bör utredas
- **Southwest är starkaste regionen** – högst omsättning och flest kunder
- **Churn är ett problem** – betydande antal kunder har inte handlat på >180 dagar
- **At Risk-segmentet** innehåller värdefulla kunder som riskerar att försvinna

## Rekommendationer

- Identifiera whitespace för att få befintliga kunder att köpa från fler kategorier
- Prioritera uppföljning av At Risk-kunder innan de churnar
- Utreda orsaken till omsättningsdippen – är det tappade storkunder?
- Säkerställa att pipeline innehåller prospects med högt potentiellt värde
- Implementera KAM-struktur för de största B2B-kunderna
- Inkludera nykundsbearbetning i säljarnas mål för att minska beroendet av få storkunder

**Rekommendationer:**
- Identifiera whitespace för tillväxt i befintlig kundbas
- Prioritera uppföljning av "At Risk"-kunder innan de churnar
- Säkerställa pipeline med högvärdiga prospects
- Utreda orsaken till den kraftiga omsättningsdippen
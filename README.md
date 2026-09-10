# Jobbannons-filter

**Namn:** Elias Paleovrachas Haag
**Repository:** [https://github.com/Gaah00/Jobbannons-filter]


## 1. Mål
En automatiserad datapipeline som hämtar jobbannonser för programmeringsspråk från JobTech API, tvättar datan och förbereder den åt framtida AI-modeller.

---

## 2. Metod
* **OOP (Arv):** Basklassen `Jobb_annons` hanterar validering. Barnklassen `Distans_jobb` ärver via `super().__init__()` och lägger till distans-status.
* **API & Rådata:** Hämtar data via `requests` och sparar till `data/raw/raw_data.csv`.
* **Datatvätt & JSON:** Läser CSV med `try/except`, sorterar bort ogiltiga rader och exporterar godkänd data till `output/clean_data.json` med GDPR-metadata.

---

## 3. Resultat
Programmet tvättade datan framgångsrikt och sorterade bort korrupta poster (t.ex. saknade orter). Den färdiga `clean_data.json` innehåller enbart validerad data med tidsstämpel och `gdpr_compliant: True`.

---

## 4. Branschanalys (Mål 1)
AI-modeller kräver ren data ("Garbage in, garbage out"). Valideringsfiltret förhindrar att felaktiga mätvärden förstör framtida modeller. Automatiska API-flöden speglar hur data-team på bolag som Volvo och Kry samlar in omvärldsdata.

---

## 5. Certifikat-koll (Mål 5)
* **Python Institute (PCEP/PCAP):** Grundläggande certifiering i Python som visar att man behärskar syntax, datatyper, funktioner och OOP.
* **Databricks Certified Associate:** Certifiering för att bearbeta och hantera data i molnmiljöer med Databricks.


---

## 6. Reflektion (Mål 8)
* **Bra:** Arv (OOP) gjorde valideringskoden ren och återanvändbar.
* **Utmaning:** Hantera tomma orter (`None`) i API-svaret.
* **Framtid:** Lägga till datavisualisering med Matplotlib (biblotek för datavisualisering i Python som används för att skapa 2D-Grafik).

---

## 7. Användning
1. Klona projektet: `git clone https://github.com/Gaah00/Jobbannons-filter`
2. Installera bibliotek: `pip install requests`
3. Kör cellerna i `projekt.ipynb`

---
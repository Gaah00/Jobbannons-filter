# Jobbannons-filter

**Namn:** Elias Paleovrachas Haag
**Repository:** [https://github.com/Gaah00/Jobbannons-filter]


## Mål
Syftet med projektet är att hämta jobbannonser från JobTech API för godkända programmeringsspråk, tvätta datan via valideringsregler och spara en AI-klar JSON-fil.

## Metod
* **API & Externa bibliotek:** Hämtar realtidsdata från JobTech API med `requests`.
* **Objektorienterad programmering (OOP):** Använder basklassen `Jobb_annons` och barnklassen `Distans_jobb` (arv) för att validera språk och plats.
* **Datahantering & GDPR:** Exporterar godkänd data till `output/clean_data.json` tillsammans med GDPR-metadata (`source`, `gdpr_compliant`, `created`).
* **Felhantering:** Använder `try/except` vid API-anrop för att förhindra krascher vid nätverksfel.

## Resultat
Programmet hämtade jobb för språken Python, Java, C++, C# och SQL. Efter datatvätt filtrerades ogiltiga poster bort och den godkända datan sparades i `output/clean_data.json`.

## Branschanalys
Projektet simulerar en automatiskt datatvätt (Data Pipeline) som förbereder rådata för AI-modeller. I AI-branschen (t.ex. hos bolag som Lovable eller JobTech) är korrekt validerad data avgörande för att förhindra felaktiga beslut i framtida modeller.

## Certifikat-koll
Relevanta yrkescertifikat för denna typ av utveckling och datahantering inkluderar:
* **Microsoft Certified: Azure AI Engineer Associate**
* **AWS Certified Developer / Cloud Practitioner**

## Reflektion
* **Vad gick bra:** Strukturerad datatvätt med OOP-metoder och en ren JSON-export med metadata.
* **Vad var svårt:** Att hantera nästlade ordböcker från API-svar utan att få felutskrifter.
* **Vad jag skulle göra annorlunda:** Lägga till en visualisering (t.ex. ett stapeldiagram med Matplotlib) över antalet jobb per språk.

## Hur man kör koden
1. Öppna `projekt.ipynb` i VS Code.
2. Kör alla celler i ordning (Cell 1 till Cell 4).
3. Den renade datafilen skapas automatiskt i `output/clean_data.json`
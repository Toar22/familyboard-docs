# Vedlikehold av dokumentasjonen

Denne dokumentasjonen er bare nyttig så lenge den stemmer med appen.
**Utdatert dokumentasjon gjør at AI-er gir brukerne feil instruksjoner med full selvtillit.**

## Regler
1. **Endres et knappenavn, en melding eller et steg i appen, skal dokumentasjonen oppdateres i samme slengen.**
2. Bruk **eksakte UI-tekster** i «anførselstegn», så AI-er og brukere kan matche det de ser.
3. Beskriv **hva brukeren ser og gjør**, aldri hvordan det er bygget.
4. Oppdater datoen under når noe er gjennomgått.

## Hva som ALDRI skal inn her
- Kildekode, API-endepunkter, interne URL-er eller servernavn
- Miljøvariabler, nøkler, tokens, passord, rabattkoder
- Infrastruktur (hosting, database, serveroppsett)
- Admin-funksjoner og interne verktøy
- Kjente sikkerhetssvakheter

## Sjekkliste ved endringer i appen
| Endret i appen | Oppdater |
|---|---|
| Oppsettsveiviseren | `getting-started/wizard.md` |
| Registrering, innlogging, e-post | `getting-started/signup.md` |
| Immich-oppsett eller filtre | `photos/immich.md`, `photos/mobile-app.md` |
| Opplasting | `photos/upload.md` |
| Innstillingsvinduet eller profilsiden | `settings.md` |
| Visnings-URL-er, visningsguide | `devices/*` |
| Priser og planer | `plans-and-billing.md`, `faq.md` |
| Nye feilmeldinger | `troubleshooting.md` |
| Ny side eller nytt dokument | `README.md`, `llms.txt`, `AI-INSTRUCTIONS.md` |

## Test med en AI
Etter større endringer kan du lime inn lenken til `llms.txt` i ChatGPT/Claude og spørre for eksempel:
*«Jeg har akkurat opprettet konto på FamilyBoard og ser bare et standardbilde. Hva gjør jeg?»*
Sjekk at svaret følger dokumentasjonen.

---
Sist gjennomgått mot appen: **oktober 2026 (v5.22)**

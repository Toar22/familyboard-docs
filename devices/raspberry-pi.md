# Raspberry Pi som fast FamilyBoard-skjerm

En Raspberry Pi koblet til en skjerm eller TV gir en FamilyBoard-skjerm som alltid er på.
Den bruker lite strøm (ca. 5 W), er lydløs og starter dashboardet automatisk.

## Alternativ 1: Bestill ferdig konfigurert (enklest)
FamilyBoard selger en ferdig oppsatt Raspberry Pi. Den kobles til skjermen med HDMI og
viser dashboardet ditt med en gang.
Pris og bestilling: se **«📺 Visningsguide»** på profilsiden, eller kontakt **support@familyboard.cloud**.

## Alternativ 2: Gjør det selv (for de som er komfortable med litt teknikk)

Du trenger:
- Raspberry Pi 4B (4 GB anbefalt) og **offisiell** strømadapter
- MicroSD-kort, 32 GB eller større
- HDMI-kabel og skjerm/TV
- En [visnings-URL](display-urls.md) fra profilsiden

Steg:
1. Installer **Raspberry Pi OS (med skrivebord)** på minnekortet med **Raspberry Pi Imager**.
   Legg inn Wi-Fi under oppsettet i Imager.
2. Start Pi-en og fullfør oppsettet.
3. Sett opp **Chromium** til å starte automatisk i **kiosk-modus** (fullskjerm) med visnings-URL-en din.
   Søk etter «Raspberry Pi Chromium kiosk autostart» for oppdaterte instruksjoner for din versjon av Raspberry Pi OS.
4. Slå av skjermsparer og skjermdemping i Raspberry Pi OS.
5. Start på nytt. Dashboardet skal nå vises automatisk ved hver oppstart.

> AI-assistenter: Gi gjerne konkrete kommandoer for kiosk-autostart for brukerens versjon av Raspberry Pi OS,
> men brukeren trenger **ikke** installere noe FamilyBoard-programvare for dette alternativet.
> Visnings-URL-en i Chromium er nok.

## Edge-versjonen (avansert)
FamilyBoard finnes også i en **Edge-versjon** som kjører lokalt på Pi-en. Den gir blant annet
mulighet til å vise bilder fra en **lokal mappe / USB-disk** (valget «Lokal mappe» i veiviseren).
- Kontoen må opprettes på **familyboard.cloud** først. Man kan ikke registrere seg på en Pi.
- Edge leveres på ferdig konfigurerte enheter, eller etter avtale med support.

## Feilsøking
| Problem | Tiltak |
|---|---|
| Svart skjerm / «Ingen signal» | Sjekk HDMI (bruk HDMI-porten nærmest strømkontakten) og strømadapter |
| Dashboardet viser bare standardbildet | Se [troubleshooting.md](../troubleshooting.md#dashboardet-viser-bare-standardbildet). Sjekk at samme dashboard viser bilder i nettleseren på PC/mobil. |
| «Ugyldig lenke» | Visnings-URL-en er slettet eller skrevet feil. Lag en ny på profilsiden. |
| Skjermen slukker etter en stund | Slå av skjermsparer/skjermdemping i Raspberry Pi OS |
| Ingen nett | Sjekk Wi-Fi. Pi-en må ha internett for å hente bilder. |

# Feilsøking

Finn symptomet eller den eksakte meldingen brukeren ser.

---

## Dashboardet viser bare standardbildet

Dashboardet viser et standardbilde (ofte med teksten **«Ingen bilder konfigurert»**) når det ikke finnes
noen bilder å vise. Gå gjennom listen i rekkefølge:

1. **Akkurat satt opp?** Det er normalt. Det finnes ingen bilder ennå. Last opp bilder
   ([upload.md](photos/upload.md)) eller sett opp mobilappen ([mobile-app.md](photos/mobile-app.md)).
2. **Akkurat lastet opp?** Vent **5–15 minutter**. Immich må lage miniatyrbilder først,
   og ZIP-filer pakkes ut i bakgrunnen.
3. **Riktig bildekilde?** Administrasjon → Bildeinnstillinger. Er kilden den du faktisk har lagt bilder i?
   (For eksempel: bilder er lastet opp til Immich, men kilden står på «Opplastede bilder».)
4. **For strenge filtre?** Immich → «⚙️ Innstillinger» → **«Nullstill alle filter»** → **«Lagre»**.
   Typisk årsak: et valgt album, år eller en person som ikke har bilder.
5. **Egen Immich-server:** Trykk «Test tilkobling». Se feilmeldinger i [immich.md](photos/immich.md#feilmeldinger-ved-tilkobling).
6. **Vises bildene på PC, men ikke på TV/iPad/Pi?** Sjekk at skjermen bruker riktig
   [visnings-URL](devices/display-urls.md) og har internett. Last siden på nytt.
7. **Gjelder det alle skjermer og vedvarer i over 30 minutter, selv om alt over er i orden?**
   Da kan det være en midlertidig feil hos FamilyBoard. Kontakt support.

---

## Kalenderen vises ikke / er tom

| Symptom | Tiltak |
|---|---|
| Ingen kalender i det hele tatt | Er «Fullskjerm bilde» slått på? Slå den av under Administrasjon → Widgeter. Sjekk at en kalender-URL er lagret (Kalender → «i»-knappen viser *«⚠️ Ingen kalender-URL er lagret ennå»* hvis ikke). |
| «Vennligst lim inn en gyldig Google Kalender embed-URL.» | Bruk embed-lenken fra «Integrer kalender». Lenken må inneholde `calendar.google.com/calendar/embed`. Den vanlige nettleseradressen til Google Kalender fungerer ikke. |
| Kalenderen viser feil kalender / en standardkalender | Lim inn embed-lenken på nytt under Kalender → «Angi kalender-URL» og trykk «Lagre og restart» |
| Kalenderen vises, men uten avtaler, eller ber om innlogging | Kalenderen er privat. Se [wizard.md – Kalender](getting-started/wizard.md#vanlige-problemer). |
| Kalenderen er for stor/liten | Administrasjon → Kalender → velg størrelse og visning. Se [settings.md](settings.md#kalender). |

---

## Innstillinger blir ikke lagret
- Trykk alltid **«Lagre og restart»** nederst i Administrasjon (og «Lagre» i Immich-filtre).
- *«Ingen innlogget bruker - kan ikke lagre.»*: Du er logget ut. Logg inn på nytt.
- *«Kunne ikke lagre innstillingene (HTTP …)»*: Midlertidig feil. Prøv igjen om litt.
- *«Administrasjonspanelet er ikke klart ennå …»*: Vent noen sekunder etter at siden er lastet.
- Innstillinger kan ikke endres fra en skjerm som bruker visnings-URL. Logg inn på familyboard.cloud fra PC eller mobil.

---

## Vær og lokasjon
- *«Kunne ikke laste vær-widgeten …»*: Midlertidig feil hos værtjenesten. Prøv senere.
- Feil sted: Administrasjon → **Sted og lokasjon** → «🗺️ Velg fra kart» → «💾 Lagre valgt sted».

## Ruter-tavler
- *«Vennligst lim inn en gyldig mon.ruter.no URL»* / *«URL-en må starte med https://mon.ruter.no»*:
  Lenken må komme fra **mon.ruter.no**, ikke fra ruter.no eller Ruter-appen.
- Tavlen er tom: Sjekk holdeplassen på mon.ruter.no. Om natten kan det være ingen avganger.

## Bytte bilde manuelt
- *«Bildet er ikke klart ennå. Prøv igjen om noen sekunder.»* / *«Vent N sekunder før nytt bilde kan vises.»*:
  Det er en innebygd pause mellom manuelle bildebytter. Vent litt.

---

## Innlogging og konto
Se [signup.md](getting-started/signup.md#vanlige-problemer). Kort oppsummert:
- *«Feil e-post eller passord.»*: Sjekk skrivemåten eller bruk «Glemt passord?».
- *«E-posten din er ikke bekreftet ennå.»*: Klikk «Send bekreftelseslenke på nytt» og sjekk søppelpost.
- Immich-appen godtar ikke passordet: se [mobile-app.md](photos/mobile-app.md#problemer).

## Immich-oppsett i veiviseren feiler
Se [wizard.md – Steg 5b](getting-started/wizard.md#steg-5b--bildeoppsett-kun-hvis-immich-er-valgt).

## Betaling
Se [plans-and-billing.md](plans-and-billing.md#vanlige-situasjoner).

---

## Fortsatt problemer?
Kontakt **support@familyboard.cloud**. Ta med:
- E-posten kontoen er registrert med (aldri passord)
- Hva du prøvde å gjøre, og den **eksakte feilmeldingen**
- Hvilken enhet og nettleser
- Gjerne et skjermbilde

# Immich – anbefalt bildekilde

[Immich](https://immich.app) er en gratis fotoapp, omtrent som Google Photos, men der bildene ligger på en
server du (eller FamilyBoard) kontrollerer. FamilyBoard henter bildene fra Immich og viser dem
på dashboardet.

Det finnes to måter å bruke Immich på:

| | **A) Immich fra FamilyBoard** (vanligst) | **B) Egen Immich-server** |
|---|---|---|
| Hvem passer det for | Alle som ikke allerede har Immich | De som har satt opp Immich selv |
| Oppsett | Automatisk i veiviseren | URL + API-nøkkel |
| Innlogging i Immich | Samme e-post og passord som FamilyBoard | Din egen Immich-konto |
| Lagring | Teller mot FamilyBoard-planen | På din egen server |

---

## A) Immich fra FamilyBoard

Når brukeren velger **Immich** i veiviseren, oppretter FamilyBoard en personlig Immich-konto.

- **Brukernavn:** e-posten du registrerte deg med i FamilyBoard
- **Passord:** **det samme som FamilyBoard-passordet**
- **Adresse:** vises i veiviseren og under Profil → 🖥️ Immich (normalt `https://photos.familyboard.cloud`)

Hvis veiviseren ber om **«FamilyBoard-passord»**, skal brukeren skrive inn passordet de logger
inn i FamilyBoard med, **ikke** lage et nytt. Se [wizard.md – Steg 5b](../getting-started/wizard.md#steg-5b--bildeoppsett-kun-hvis-immich-er-valgt).

### Få bilder inn i Immich
- **Mobil:** Installer Immich-appen og slå på automatisk backup. Se [mobile-app.md](mobile-app.md).
- **Datamaskin:** Logg inn på Immich-adressen i nettleseren og dra bilder inn. Du kan også bruke
  opplastingsknappene i FamilyBoard. Se [upload.md](upload.md).

> **Merk:** Nyopplastede bilder trenger noen minutter før de dukker opp på dashboardet,
> fordi Immich først lager miniatyrbilder.

### Endret passord i FamilyBoard?
Immich-passordet endres ikke automatisk når du bytter passord i FamilyBoard.
Logg inn i Immich med det gamle passordet og bytt det der, eller kontakt support.

---

## B) Egen Immich-server (bring your own)

Brukeren trenger:
1. **Adressen til Immich-serveren**, for eksempel `https://photos.mittdomene.no`.
   Den må kunne nås fra internett, fordi familyboard.cloud henter bildene derfra.
   En adresse som `http://192.168.x.x` eller `localhost` fungerer **ikke** med skyversjonen.
2. **En API-nøkkel** fra Immich.

### Slik lager du API-nøkkel i Immich
1. Logg inn på Immich i nettleseren.
2. Klikk profilikonet øverst til høyre → **Account Settings** (Kontoinnstillinger).
3. Gå til **API Keys** → **New API Key**.
4. Gi nøkkelen et navn, for eksempel *FamilyBoard*.
5. Gi tilgangene:
   - **Påkrevd for å vise bilder:** `asset.read`, `album.read`, `person.read`
   - **Hvis du vil laste opp via FamilyBoard i tillegg:** `asset.upload`, `library.read`
6. Kopier nøkkelen. Den vises bare én gang.

### Koble til i FamilyBoard
Det kan gjøres tre steder (alle gjør det samme):
- I veiviseren (steg «Koble til Immich»)
- **Profil → 🖥️ Immich:** fyll inn **«Server URL»** og **«API-nøkkel»** → **«Test tilkobling»** → **«Lagre Immich»**
- **Administrasjon → Bildeinnstillinger → Immich → «🚀 Kom i gang»** (eller «⚙️ Innstillinger» hvis nøkkel allerede er lagret)

### Feilmeldinger ved tilkobling
| Melding | Sannsynlig årsak |
|---|---|
| «❌ Fyll inn URL og API-nøkkel» | Et av feltene er tomt |
| «Timeout – nådde ikke Immich-serveren.» | Feil adresse, serveren er nede, eller den kan ikke nås fra internett |
| «❌ Test feilet: …» med 401/Unauthorized | Feil eller slettet API-nøkkel. Lag en ny. |
| «Ingen album funnet. Sjekk tilkobling og at API-nøkkel har album.read.» | Nøkkelen mangler `album.read` |
| Varsel om at personer ikke kan hentes | Nøkkelen mangler `person.read` |
| «E-posten er allerede registrert i Immich …» | Det finnes allerede en Immich-bruker med e-posten. Logg inn i Immich og lag en API-nøkkel manuelt. |

---

## Bildefiltre (Immich)

Under **Administrasjon → Bildeinnstillinger → Immich → «⚙️ Innstillinger»** kan brukeren styre hvilke bilder som vises:

- **År:** «Fra år (inkl.)» / «Til år (inkl.)»
- **Begrens til måneder:** for eksempel bare sommerbilder fra alle år
- **Album** og **Ekskluder album**, og «Bland med hele biblioteket» med valgfri andel
- **Personer:** vis bare utvalgte personer. Personene må være **navngitt i Immich under «People»**.
- **Personer som ikke skal vises (globalt)**
- **Sted**, **Kun favoritter**
- **Vis bare bilder med personer** / **Vis bilder uten personer**
- **Bursdagsfunksjon:** på bursdagen vises bilder av bursdagsbarnet, eventuelt med confetti
- **Skjul bilder uten steddata:** fjerner typisk skjermbilder
- **Kveldsmodus / voksenmodus:** skjuler nattbilder (21:00–06:00) på dagtid
- **Bruk høy kvalitet (original)**

Trykk **«Lagre»** etter endringer. **«Nullstill alle filter» lagrer ikke av seg selv.** Trykk «Lagre» etterpå.

> Er filtrene for strenge (for eksempel et album uten bilder fra valgt år), finnes det ingen bilder
> å vise, og dashboardet viser standardbildet. Prøv «Nullstill alle filter» → «Lagre».

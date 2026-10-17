# Oppsettsveiviseren («Kom i gang»)

Etter første innlogging møter brukeren en veiviser med disse stegene
(fremdriftslinjen øverst viser hvor man er):

**Velkommen → Kalender → Lokasjon → Ruter → Bildekilde → (Bildeoppsett) → Ferdig**

Generelt:
- Alle steg kan hoppes over med **«Hopp over»**, og man kan gå tilbake med **«← Tilbake»**.
- **Alt kan endres senere** fra innstillingene på dashboardet. Brukeren trenger ikke få alt perfekt i veiviseren.
- Fremdriften lagres. Lukker brukeren nettleseren, fortsetter veiviseren der de slapp.

---

## Steg 1 – Velkommen

Kort oversikt over hva som skal settes opp (kalender, lokasjon, bildekilde).
Trykk **«Kom i gang →»**.

---

## Steg 2 – Kalender: «Vil du vise kalender?»

To valg:

| Valg | Resultat |
|---|---|
| **Ja, med kalender** | Dashboardet viser en Google Kalender ved siden av bildene |
| **Nei, fullskjerm bilder** | Bildene dekker hele skjermen |

Velger brukeren **Ja**, dukker feltet **«Google Kalender embed-lenke»** opp.

### Slik finner du embed-lenken i Google Kalender
1. Åpne Google Kalender **på en datamaskin** (embed-innstillingen finnes ikke i mobilappen).
2. Tannhjul → **Innstillinger**.
3. I venstremenyen, under «Innstillinger for mine kalendere», velg kalenderen du vil vise.
4. Bla ned til **«Integrer kalender»**.
5. Kopier enten **«Offentlig URL til denne kalenderen»** eller hele **«Innebyggingskode»** (`<iframe …>`).
   FamilyBoard godtar begge deler og plukker selv ut det som trengs.
6. Lim inn i feltet og trykk **«Neste →»**.

Veiviseren har også en knapp: **«Åpne Google Kalender embed-hjelp →»**.

### Vanlige problemer
- **Kalenderen vises tom eller med «Du har ikke tilgang»:** Kalenderen er privat.
  Google viser bare innebygde kalendere for innloggede brukere med tilgang, eller hvis
  kalenderen er gjort offentlig (Innstillinger → kalenderen → «Tilgangstillatelser for aktiviteter»
  → «Gjør tilgjengelig for offentligheten»). Gjør brukeren oppmerksom på at offentlig betyr at alle
  med lenken kan se avtalene. Et alternativ er å vise bare «ledig/opptatt».
- **Flere kalendere (familiemedlemmer):** Bruk Googles embed-hjelp (lenken over) til å lage én
  embed-kode som viser flere kalendere samtidig, og lim den inn.
- **Bruker har iCloud- eller Outlook-kalender:** Veiviseren støtter Google Kalender-embed.
  En vanlig løsning er å abonnere på iCloud/Outlook-kalenderen inne i Google Kalender
  («Andre kalendere» → «Fra nettadresse») og så vise den derfra.

---

## Steg 3 – Lokasjon: «Hvor bor du?»

Brukeren **klikker på kartet** der de bor. Stedsnavnet vises under kartet.
Lokasjonen brukes til **vær** og **soloppgang/solnedgang**.
Trykk **«Neste →»** (knappen blir aktiv først når et sted er valgt).

Tips: Zoom inn før du klikker for å treffe riktig sted.

---

## Steg 4 – Ruter: «Vil du vise kollektivavganger?»

FamilyBoard kan vise **to avgangstavler fra Ruter** (kollektivtrafikk i Oslo og Viken)
nede til høyre på dashboardet, for eksempel to ulike holdeplasser.

Tre måter å gå videre på:
- **«Hopp over»** – ingen avgangstavler.
- **«Bruk default (Oslo)»** – en standard Oslo-holdeplass, fin for å se hvordan det ser ut.
- **Egne holdeplasser** – lim inn URL-er og trykk **«Neste →»**.

### Slik finner du riktig URL
1. Gå til **https://mon.ruter.no**.
2. Søk opp og velg holdeplassen.
3. Kopier hele adressen fra adressefeltet i nettleseren.
4. Lim inn i **«Ruter-widget 1 (venstre)»** og eventuelt **«Ruter-widget 2 (høyre)»**.
   Begge feltene er valgfrie.

### Feilmeldinger
- **«URL-en må starte med https://mon.ruter.no»** – brukeren har limt inn noe annet
  (for eksempel en lenke fra ruter.no eller Ruter-appen). Bruk mon.ruter.no.
- **«Ugyldig URL. Vennligst kontroller og prøv igjen.»** – URL-en er ufullstendig. Kopier den på nytt.

Bor brukeren utenfor Ruters område, er det bare å hoppe over steget.

---

## Steg 5 – Bildekilde: «Velg bildekilde»

| Valg | Passer for | Merk |
|---|---|---|
| **Immich** ★ Anbefalt | De fleste. FamilyBoard setter opp en personlig bildelagring automatisk, eller man kobler til sin egen Immich-server | Synk fra mobil med Immich-appen, filtrering på album/personer/år. Se [immich.md](../photos/immich.md) |
| **Last opp bilder** | De som vil komme raskt i gang uten app | Opplasting i nettleseren (enkeltbilder eller ZIP). 10 GB inkludert på gratisplanen. Se [upload.md](../photos/upload.md) |
| **Lokal mappe** | Kun Raspberry Pi / Edge-installasjon | **Fungerer ikke** i nettleser-/skyversjonen. Se [raspberry-pi.md](../devices/raspberry-pi.md) |

> FamilyBoard er **ikke** en backup-løsning. Brukeren bør alltid ha originalbildene lagret et annet sted.

Velger brukeren **Immich**, kommer et ekstra steg (Bildeoppsett). Velger de noe annet, går de rett til «Ferdig».

---

## Steg 5b – Bildeoppsett (kun hvis Immich er valgt)

Hva brukeren ser, avhenger av situasjonen:

### A) «Bildelagring klar» ✅
Lagringen er allerede satt opp automatisk. Brukeren ser en lenke til sin Immich-side
og kan trykke **«Neste →»**. Ingenting mer å gjøre.

### B) «Sett opp bildelagring» – brukeren må skrive inn passord
Skjemaet **«Koble til bildelagring»** viser e-posten og ber om **«FamilyBoard-passord»**.

- Skriv inn **det samme passordet som du logger inn i FamilyBoard med**. Det er **ikke** et nytt passord.
- Trykk **«Koble til Immich»**.

| Melding | Betydning / tiltak |
|---|---|
| «⏳ Oppretter Immich-konto…» | Vent. Det kan ta noen sekunder. |
| «✅ Immich-konto opprettet!» | Ferdig. Trykk «Neste →». |
| «❌ Feil passord. Skriv inn passordet du bruker til å logge inn i FamilyBoard …» | Brukeren skrev et nytt eller annet passord. Bruk innloggingspassordet. |
| «❌ Passordet må være minst 8 tegn» | Feil passord er skrevet inn (innloggingspassordet er alltid minst 8 tegn). |
| «⚠️ Kontoen ble opprettet, men bibliotekskobling feilet …» | Delvis vellykket. Brukeren kan fullføre veiviseren og prøve igjen senere fra **Profil → 🖥️ Immich** eller **Administrasjon → Bildeinnstillinger → Immich**. |
| «… API-nøkkel ble ikke opprettet automatisk …» | Kontoen finnes, men koblingen må fullføres fra innstillingene på dashboardet. |

### C) «Koble til Immich» – egen Immich-server
For brukere som har sin **egen** Immich-installasjon. Se
[immich.md → Egen Immich-server](../photos/immich.md#egen-immich-server-bring-your-own).
Feltene er **«Immich server URL»** og **«API-nøkkel»**, og man må trykke **«Test tilkobling»**
før «Neste →» blir aktiv.

---

## Steg 6 – Ferdig: «Du er klar! 🎉»

Her får brukeren tips tilpasset bildekilden (hvordan laste opp de første bildene), og to valgfrie guider:
- **«📖 Se mobil-oppsett»** – koble Immich-appen på mobilen så nye bilder synkes automatisk.
  Se [mobile-app.md](../photos/mobile-app.md).
- **«📖 Se iPad-oppsett»** – bruke en iPad som digital fotoramme.
  Se [ipad-and-tv.md](../devices/ipad-and-tv.md).

Trykk **«Gå til dashboardet →»**.

### Hvis dashboardet bare viser et standardbilde
Det er normalt rett etter oppsett. Det finnes ingen bilder ennå, eller de nyopplastede bildene
behandles fortsatt. Se [troubleshooting.md](../troubleshooting.md#dashboardet-viser-bare-standardbildet).

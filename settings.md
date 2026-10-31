# Innstillinger etter oppsett

FamilyBoard har to steder for innstillinger:
- **Administrasjon** (på dashboardet): hva som vises og hvordan
- **Profil / Min konto**: konto, passord, Immich, plan og visnings-URL-er

## Åpne innstillingene
1. Gå til dashboardet (logget inn på familyboard.cloud).
2. **Klikk hvor som helst på skjermen.** En blå **«Administrasjon»**-knapp dukker opp nede til høyre i noen sekunder.
3. Klikk på den. Innstillingsvinduet åpnes.
4. Etter endringer: trykk den grønne **«Lagre og restart»** nederst.

Innstillingsvinduet lukkes med X, Esc eller ved å klikke utenfor.
Lenken **«Min konto →»** øverst til høyre går til profilsiden.

> Innstillinger gjøres på en enhet der du er logget inn (PC, mobil). Skjermer som bruker en
> [visnings-URL](devices/display-urls.md) oppdateres automatisk.

---

## Administrasjon – faner

### Bildeinnstillinger
- **Bildekilde** (én aktiv om gangen): **Immich ★ Anbefalt**, **Opplastede bilder** eller **Lokal harddisk** (kun Raspberry Pi med den eldre Edge-versjonen)
- Immich-innstillinger og filtre: se [photos/immich.md](photos/immich.md)
- Opplasting: se [photos/upload.md](photos/upload.md)
- **Oppdateringsintervall:** hvor ofte bildet byttes (1–30 min, 5 min er standard). «Annet» gir valgfritt antall minutter.

### Sted og lokasjon
Velg sted fra listen eller **«🗺️ Velg fra kart»** → klikk på kartet → **«💾 Lagre valgt sted»**.
Brukes til vær (Yr) og soloppgang/solnedgang.

### Widgeter
- **Ruter 1 (venstre)** / **Ruter 2 (høyre)** → **«Sett URL»**: lim inn en lenke fra mon.ruter.no.
  Tips: Velg holdeplasser uten tog og horisontal tavlevisning.
- Av/på-brytere: **Vis klokke**, **Vis YR** (vær), **Vis klesråd**, **Vis sted** (hvor bildet er tatt),
  **Vis tidspunkt / år-måned**, **Vis fremdriftslinje for bildebytte**, **Vis meldinger på skjermen**, **Fullskjerm bilde**
- **Egen widget 1–5 (beta):** vis en ekstern nettside (iframe) eller data fra et API i en egen boks
- Enkelte widgeter krever betalt plan. Se [plans-and-billing.md](plans-and-billing.md).

### Design (beta)
Egne fargeprofiler for bakgrunn, klokke, vær, kalender, rammer m.m., og eget bakgrunnsbilde (maks ca. 8 MB).
Standardprofilen kan ikke endres. Lag en ny profil for å tilpasse.

### Kalender
- **Størrelse:** X-large (ukesvisning, 100 % zoom), Large (med kollektivtavler), Medium, Small
- **Visning:** Oversikt / Uke / Måned
- **Fullskjerm kalender**
- **«Angi kalender-URL»:** lim inn embed-lenke fra Google Kalender. «i»-knappen viser hvilken URL som er lagret.

**Slik får du en pen kalender** (se [best-practices.md – anbefalte innstillinger](best-practices.md#1c-vis-alle-kalenderne-samlet-i-familyboard--våre-anbefalte-innstillinger)):
1. Google Kalender (på PC) → Innstillinger → velg kalender → **«Integrer kalender»** → **«Tilpass»**.
2. Fjern haken på alle «Vis»-valgene (Tittel, Navigeringsknapper, Dato, Utskriftsikon, Åpne menyen, Kalenderliste, Tidssone, Kantlinje).
3. Standardvisning **Oversikt**, uken starter på **Mandag**, språk Norsk (bokmål).
4. Huk av kalenderne som skal vises.
5. Kopier innebyggingskoden og lim inn i FamilyBoard.

Lenken må inneholde `calendar.google.com/calendar/embed`.
Andre kalendere (iCloud, Outlook) må først legges inn i Google Kalender. Se [faq.md](faq.md).

---

## Profil / Min konto
Menyen til venstre:
- **👤 Personlig info:** navn, mobil, e-post, adresse
- **🔑 Passord:** bytt passord (minst 8 tegn). Merk at Immich-passordet ikke endres automatisk.
- **🖥️ Immich:** status, server-URL, API-nøkkel, **«📱 Koble mobilen»**
- **💾 Plan:** aktiv plan, pris, lagringsbruk, **«⚡ Endre plan»**, **«🔧 Administrer abonnement»** (betalingskort og kvitteringer), **«↻ Synkroniser plan»**
- **🔗 URLer:** visnings-URL-er for skjermer. Se [devices/display-urls.md](devices/display-urls.md).
- **⚠️ Konto:** sletting av konto (gjøres foreløpig via support). Se [faq.md](faq.md).

Øverst: **«← Dashboard»**, **«📺 Visningsguide»**, **«Logg ut»**.

# Anbefalt oppsett – slik får du mest ut av FamilyBoard

Dette er anbefalingene våre, basert på hvordan vi selv bruker FamilyBoard hjemme.
Ingenting her er påkrevd. Det er tips for å få en skjerm hele familien faktisk bruker.

> **Til AI-assistenter:** Bruk denne guiden når brukeren spør «hvordan bør jeg sette det opp?»,
> «hva anbefaler dere?» eller vil ha et godt utgangspunkt. Ta det i små porsjoner. Spør hva brukeren
> allerede har (Google Kalender? iPhone/Android? hvor mange i familien?) og start med kalender og bilder.
> Mange av stegene skjer i **Google Kalender**, **Spond** og **Immich**, ikke i FamilyBoard.
> Si tydelig hvilken app brukeren skal være i.

**Kortversjon:**
1. Samle hele familien i **én familiekalender** i Google Kalender, inkludert Spond, skole og barnehage.
2. Alle i familien installerer **Immich-appen** og laster opp bilder automatisk.
3. **Rydd bildene** med Immich: legg uønskede bilder i et eget album som utelates, og vis bare bilder med personer.
4. Legg inn **navn og bursdag** på viktige personer i Immich, og slå på **bursdagsfunksjonen**.
5. **Del album** med besteforeldre og andre i familien.
6. Bildebytte hvert **5. minutt**, kalender i **ukevisning**.
7. Finjuster utseendet i **Design-modus**.

---

## 1. Kalender: én familiekalender for alt

Målet er å få **mest mulig** inn i én familiekalender som vises på skjermen.

> **Bruker du Apple-kalender, Outlook eller noe annet?** Du trenger ikke bytte.
> Lag en egen **gratis** Google-kalender (eller Google-konto) **bare for skjermen**, og link de kalenderne
> dere allerede bruker inn i den. Da fortsetter alle å bruke det de har i dag, uten å merke noe,
> mens skjermen viser alt samlet.

### 1a. Lag en felles familiekalender i Google Kalender
1. Google Kalender på PC → **«+»** ved «Andre kalendere» → **«Opprett ny kalender»** → kall den f.eks. *Familien*.
2. Del den med alle voksne i familien: Innstillinger for kalenderen → **«Del med bestemte personer»** →
   legg til e-postene og gi tilgang **«Gjøre endringer i aktiviteter»**.
3. Alle legger felles avtaler (middager, besøk, ferier) i *Familien*-kalenderen.

### 1b. Ta inn de andre kalenderne
| Kilde | Slik kobler du den inn i Google Kalender |
|---|---|
| **Hver voksens egen Google-kalender** | Del den med de andre (se over), eller vis den sammen med familiekalenderen i embed-koden (steg 1c) |
| **Spond** (idrett og aktiviteter) | Spond-appen har kalendersynkronisering som gir en kalenderlenke (iCal). I Google Kalender: «Andre kalendere» → **«Fra nettadresse»** → lim inn lenken. |
| **Skole og barnehage** | Sjekk først om appen (f.eks. Vigilo, MyKid, Kidplan, Visma/Transponder) tilbyr kalenderabonnement eller eksport. Legg det inn med «Fra nettadresse». |
| **E-post fra skole/barnehage** | Har de ikke kalenderlenke, kan e-postene automatiseres til kalenderhendelser, for eksempel med Gmail-filtre og en automatiseringstjeneste eller AI-assistent som lager kalenderhendelser fra e-post. Alternativt legges viktige datoer inn manuelt i *Familien*. |
| **iCloud- eller Outlook-kalender** | Publiser den som lenke i iCloud/Outlook og legg den inn med «Fra nettadresse» |

> Kalendere lagt inn med «Fra nettadresse» oppdateres av Google, typisk noen ganger i døgnet, ikke umiddelbart.

### 1c. Vis alle kalenderne samlet i FamilyBoard
1. Google Kalender → Innstillinger → velg *Familien* → **«Integrer kalender»** → **«Tilpass»**.
2. **Huk av kalenderne** som skal vises (familie, hver voksen, Spond, skole). De får hver sin farge.
   **Fjern haken** på kalendere som ikke skal på skjermen, f.eks. jobbkalendere, helligdager eller fødselsdager du ikke vil se.
3. Velg en visning med **tiden nedover**, f.eks. **«Uke»**. Det synes vi er finest. Prøv gjerne «Oversikt» også, og se hva som passer skjermen.
4. **Fjern alt annet** for et rent utseende: Tittel, Kantlinje (ramme), Navigasjon, Dato, Utskrift, Meny,
   Kalenderliste og Tidssone. Ta bort alt som ikke er selve kalenderen.
5. Kopier innebyggingskoden (eller bare lenken) og lim den inn i FamilyBoard: **Administrasjon → Kalender → «Angi kalender-URL»**.
6. Sett samme **Visning** i FamilyBoard, og størrelse **X-large**, eller **Large** hvis du også har Ruter-tavler.

### 1d. Logg inn i Google på skjermen
Familiekalenderen er privat, og det skal den være. For at den skal vises på skjermen, må nettleseren
på skjermen være **logget inn på Google-kontoen** som har tilgang til kalenderen:
- **Raspberry Pi:** Åpne Chromium én gang og logg inn på Google. Se [devices/raspberry-pi.md](devices/raspberry-pi.md).
- **iPad:** Logg inn på Google-kontoen på iPaden (i Safari eller via iPad-innstillingene), og åpne deretter FamilyBoard.
- Bruker du en egen Google-konto bare for skjermen (se over), er det den du logger inn med.
  Da ligger ingen andre private data på skjermen.

Ser du «Du har ikke tilgang» eller en tom kalender, er det nesten alltid fordi nettleseren på skjermen ikke er logget inn.

Se også [settings.md – Kalender](settings.md#kalender).

---

## 2. Bilder: hele familien i Immich

### 2a. Alle laster opp automatisk
- Alle i familien installerer **Immich-appen** og logger inn på **samme FamilyBoard-konto**.
  Det er det enkleste: alle bildene havner på ett sted og vises på skjermen.
  Se [photos/mobile-app.md](photos/mobile-app.md).
- Slå på **bakgrunnsbackup** på alle telefonene.

### 2b. Last opp det gamle fotoarkivet
- Rydd gjerne først. Slett dubletter, skjermbilder og mislykkede bilder.
- Last opp hele familiealbumet: fra PC via Immich i nettleseren, eller som **ZIP-fil** via FamilyBoard.
  Se [photos/upload.md](photos/upload.md).
- Gi Immich litt tid etter store opplastinger. Ansiktsgjenkjenning og miniatyrbilder kan ta timer for store arkiv.

### 2c. Styr hva som vises på skjermen
Skjermen henger ofte i et rom der gjester også ser den. Slik holder du den hyggelig:

1. **Lag et album for bilder som ikke skal vises**, f.eks. *Ikke på skjerm*.
2. Bruk **søket i Immich** (det forstår vanlig tekst) til å finne bilder du ikke vil ha på skjermen,
   for eksempel bilder fra bading, stranden eller badekaret, kvitteringer eller dokumenter. Legg dem i *Ikke på skjerm*.
3. I FamilyBoard: **Administrasjon → Bildeinnstillinger → Immich → «⚙️ Innstillinger»** →
   **«Ekskluder album»** → velg *Ikke på skjerm* → **«Lagre»**.
4. Slå på **«Vis bare bilder med personer»**. Da forsvinner skjermbilder, handlelister, bilder av ting man skulle huske
   og andre bilder som ikke er hyggelige minner.
5. Vurder også **«Skjul bilder uten steddata»** (fjerner typisk skjermbilder) og **«Kveldsmodus»**
   (skjuler nattbilder på dagtid).

Se alle filtrene i [photos/immich.md – Bildefiltre](photos/immich.md#bildefiltre-immich).

---

## 3. Personer og bursdager

1. I Immich: åpne **«People»** (Personer). Immich har gruppert ansikter automatisk.
2. Gi **navn** til familie, venner og andre viktige personer.
3. Legg inn **fødselsdato** på personen (åpne personen → rediger → fødselsdato).
4. I FamilyBoard: Immich → «⚙️ Innstillinger» → **«Slå på bursdagsfunksjon»**,
   eventuelt også **«Bruk confetti ved bursdager»** → **«Lagre»**.

På bursdagen viser skjermen bare bilder av bursdagsbarnet, fra hele biblioteket. Det blir fort et samtaleemne.

> Personer må være navngitt i Immich for å kunne velges i filtrene og for at bursdagsfunksjonen skal virke.

---

## 4. Del bilder med besteforeldre og resten av familien

Har besteforeldre (eller andre) også FamilyBoard, kan dere dele bilder begge veier:

1. I Immich: søk opp personen, f.eks. *Bestemor* (fra People), eller lag et album *Med bestemor og bestefar*
   med bildene dere har sammen.
2. **Del albumet** med bestemor og bestefars Immich-bruker (Album → Del → velg bruker).
3. Bestemor og bestefar gjør det samme motsatt vei: de deler et album med bilder der dere er med.
4. Delte album kan velges i FamilyBoard-filtrene (**«Album»**), eller blandes inn med
   **«Bland med hele biblioteket»**.

Da får besteforeldrene bildene av barnebarna rett på skjermen sin, uten å sende bilder på meldinger.

---

## 5. Visning og utseende

| Innstilling | Vår anbefaling | Hvor |
|---|---|---|
| Bildebytte | **5 minutter** | Administrasjon → Bildeinnstillinger → Oppdateringsintervall |
| Kalendervisning | **Uke** | Administrasjon → Kalender |
| Kalenderstørrelse | **X-large**, eller **Large** med Ruter-tavler | Administrasjon → Kalender |
| Klokke og vær | På | Administrasjon → Widgeter |
| Sted og år på bildet | På. Det gir gode «hvor var dette?»-samtaler. | Administrasjon → Widgeter |

### Design-modus: gjør skjermen din egen
1. **Administrasjon → Design** → slå på **«Design-modus»**.
2. Lag en **ny profil** (standardprofilen kan ikke endres).
3. **Dra og endre størrelse på boksene** (klokke, vær, kalender, tavler) direkte på dashboardet til det passer skjermen.
4. Juster farger og eventuelt bakgrunnsbilde, og lagre.

Design-modus er i beta. Det er lurt å ta et bilde av skjermen før du gjør store endringer.

---

## 6. Skjermen

- Bruk en **fast skjerm som alltid er på**: Raspberry Pi med skjerm/TV, eller en iPad på vegg eller stativ.
  Se [devices/](devices/).
- Plasser den der familien faktisk passerer: kjøkken, gang eller ved spisebordet.
- Bruk en egen [visnings-URL](devices/display-urls.md) per skjerm, så kan du stenge én uten å påvirke de andre.

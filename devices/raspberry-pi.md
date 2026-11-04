# Raspberry Pi som fast FamilyBoard-skjerm

En Raspberry Pi koblet til en skjerm eller TV gir en FamilyBoard-skjerm som alltid er på.
Den bruker lite strøm (ca. 5 W), er lydløs og starter dashboardet automatisk.

## Alternativ 1: Bestill ferdig konfigurert (enklest)
FamilyBoard selger en ferdig oppsatt Raspberry Pi. Den kobles til skjermen med HDMI og
viser dashboardet ditt med en gang.
Pris og bestilling: se **«📺 Visningsguide»** på profilsiden, eller kontakt **support@familyboard.cloud**.

### Flytte skjermen eller bytte WiFi (ferdig konfigurert Pi)
Pi-en kobler seg automatisk til WiFi-nett den kjenner fra før, og til nettverkskabel.
I et nytt hjem eller med nytt WiFi-passord setter du den opp med mobilen:

1. Sett Pi-en i strøm på det nye stedet og vent **1–2 minutter**. Finner den ikke et kjent nett,
   viser skjermen **«FamilyBoard Recovery»** med navnet på et eget oppsettsnett.
2. På mobilen: koble til WiFi-nettet **FamilyBoard-Setup-XXXX** (XXXX er fire tegn som står på skjermen).
   Passordet er **familyboard**. Sier mobilen at nettet ikke har internett, velg å bli tilkoblet likevel.
3. Siden **«📺 FamilyBoard – WiFi»** åpnes av seg selv. Gjør den ikke det, skriv **http://192.168.4.1** i nettleseren.
4. Velg ditt WiFi i listen under **«Nettverk»**. Står det ikke der (skjult nett), skriv navnet i feltet under.
   Skriv WiFi-passordet og trykk **«Koble til»**.
5. Koble mobilen tilbake til ditt vanlige WiFi. Innen ca. 1 minutt viser skjermen dashboardet.

- Kommer **FamilyBoard-Setup-XXXX** tilbake etter 1–3 minutter, var nettverksnavnet eller passordet feil.
  Koble til igjen og prøv på nytt.
- Oppsettsnettet startes bare når Pi-en slås på uten kjent nett. Er WiFi-en byttet mens Pi-en står på,
  ta ut strømmen og sett den i igjen.
- Med **nettverkskabel** i ruteren trengs ingen oppsett.
- Pi-en husker også det gamle nettet, så den virker når den flyttes tilbake.

## Alternativ 2: Gjør det selv (for de som er komfortable med litt teknikk)

Du trenger:
- Raspberry Pi 4B (4 GB anbefalt) og **offisiell** strømadapter
- MicroSD-kort, 32 GB eller større
- HDMI-kabel og skjerm/TV
- En [visnings-URL](display-urls.md) fra profilsiden

### Enklest: FamilyBoard-installeren
Installeren setter opp alt automatisk: fullskjerm, oppstart, oppsettsnett for nytt WiFi
og nattlig omstart. Den krever ingen GitHub-konto. Følg steg 1 under (installer OS med
SSH og WiFi), logg inn på Pi-en og kjør:

```bash
sudo apt-get install -y git
git clone https://github.com/Toar22/familyboard-edge.git ~/familyboard-edge
cd ~/familyboard-edge
sudo KIOSK_URL="https://familyboard.cloud/d/DIN-KODE" bash install_thin_pi.sh
sudo reboot
```

Mer om oppdatering, Google-kalender og nytt WiFi står i
[installerens veiledning](https://github.com/Toar22/familyboard-edge#readme).
Vil du heller gjøre det for hånd, følg stegene under.

### Steg 1 – Installer Raspberry Pi OS
1. Last ned **Raspberry Pi Imager** på PC/Mac (raspberrypi.com/software).
2. Velg *Raspberry Pi 4*, **Raspberry Pi OS (64-bit)** med skrivebord, og minnekortet.
   Bruk Raspberry Pi OS, ikke Ubuntu. På Ubuntu sitt standard-skrivebord blir fullskjerm ofte
   ufullstendig (panel og verktøylinje vises, eller bare halve skjermen brukes).
3. Under «Rediger innstillinger»: sett brukernavn og passord, **Wi-Fi** (navn og passord), tidssone *Europe/Oslo*, og slå gjerne på **SSH**.
4. Skriv til kortet, sett det i Pi-en, koble til skjerm (bruk HDMI-porten nærmest strømkontakten) og strøm.

### Steg 2 – Slå av skjermsparer
Åpne Terminal på Pi-en og kjør:
```bash
sudo raspi-config
```
Velg **Display Options → Screen Blanking → No**, og avslutt med *Finish*.

### Steg 3 – Logg inn i Google i Chromium (hvis kalenderen er privat)
Åpne Chromium på Pi-en én gang, og logg inn på Google-kontoen som har tilgang til familiekalenderen.
Det gjør at en privat Google-kalender vises på skjermen. Se [troubleshooting.md – Kalender](../troubleshooting.md#kalenderen-vises-ikke--er-tom).

### Steg 4 – Start FamilyBoard automatisk i fullskjerm
Nyere Raspberry Pi OS (Bookworm, 2024 og senere) bruker skrivebordet *labwc*. Kjør i Terminal
(bytt ut lenken med din egen visnings-URL):
```bash
mkdir -p ~/.config/labwc
echo 'chromium --kiosk --noerrdialogs --disable-infobars --disable-session-crashed-bubble https://familyboard.cloud/d/DIN-KODE &' >> ~/.config/labwc/autostart
```
Heter programmet `chromium-browser` på din versjon (sjekk med `which chromium chromium-browser`), bruk det navnet i stedet.

**Kjør kommandoen bare én gang.** Den legger til en linje hver gang den kjøres, og to linjer gir to
nettleservinduer oppå hverandre. Sjekk fila med:
```bash
cat ~/.config/labwc/autostart
```
Det skal bare være én linje som starter `chromium`. Fjern eventuelle duplikater med `nano ~/.config/labwc/autostart`.

Ikke legg til `--window-size` eller `--window-position`. Da viser Chromium verktøylinjen igjen.

### Steg 5 – Start på nytt
```bash
sudo reboot
```
Dashboardet skal nå åpnes i fullskjerm ved hver oppstart.

- **Avslutte fullskjerm:** `Alt+F4` med tastatur tilkoblet.
- **Skru skjermen av om natten:** Mange TV-er/skjermer har innebygd av/på-timer. Det er enklest.

> AI-assistenter: Kommandoene over gjelder Raspberry Pi OS Bookworm med labwc. Bruker brukeren en eldre
> versjon (X11/LXDE eller Wayfire), tilpass autostart-metoden. Brukeren trenger **ikke** installere
> FamilyBoard-programvare for dette alternativet. Chromium med visnings-URL-en er nok.

## Eldre Edge-versjon (fases ut)
Noen tidligere leverte Pi-er kjører en eldre **Edge-versjon** med FamilyBoard installert lokalt.
Den er den eneste som støtter bildekilden **«Lokal mappe»** (USB-disk).
- Edge-versjonen tilbys ikke for nye oppsett. Nye Pi-skjermer, også de ferdig konfigurerte, viser
  bare en visnings-URL som beskrevet over. Alt hentes fra familyboard.cloud.
- Bruk **Immich** som bildekilde i stedet for «Lokal mappe».
- Kontoen må alltid opprettes på **familyboard.cloud**. Man kan ikke registrere seg på en Pi.

## Feilsøking
| Problem | Tiltak |
|---|---|
| Svart skjerm / «Ingen signal» | Sjekk HDMI (bruk HDMI-porten nærmest strømkontakten) og strømadapter |
| Dashboardet viser bare standardbildet | Se [troubleshooting.md](../troubleshooting.md#dashboardet-viser-bare-standardbildet). Sjekk at samme dashboard viser bilder i nettleseren på PC/mobil. |
| «Ugyldig lenke» | Visnings-URL-en er slettet eller skrevet feil. Lag en ny på profilsiden. |
| Skjermen slukker etter en stund | Slå av skjermsparer/skjermdemping i Raspberry Pi OS |
| Dashboardet fyller bare halve skjermen | Pi-en har to HDMI-kabler tilkoblet og bruker dem som én bred skjerm. Bruk bare én HDMI-kabel, eller still inn speiling under skjerminnstillingene. |
| Panel, menylinje eller Chromium-verktøylinje vises | Chromium er ikke i kiosk-modus. Sjekk at autostart-linjen har `--kiosk` og ikke `--window-size`. På Ubuntu: bytt til Raspberry Pi OS. |
| Feilmelding eller et annet vindu bak dashboardet | Autostart starter Chromium to ganger. Se «Kjør kommandoen bare én gang» i steg 4. |
| Kalenderen er tom eller ber om innlogging | Logg inn på Google i Chromium på Pi-en (steg 3). Se [troubleshooting.md – Kalender](../troubleshooting.md#kalenderen-vises-ikke--er-tom). |
| Ingen nett / skjermen viser «FamilyBoard Recovery» | Pi-en finner ikke et kjent WiFi. Ferdig konfigurert Pi: følg [Flytte skjermen eller bytte WiFi](#flytte-skjermen-eller-bytte-wifi-ferdig-konfigurert-pi). Selvbygd Pi: sett WiFi i Raspberry Pi OS (WiFi-ikonet øverst til høyre), eller bruk nettverkskabel. |
| Finner ikke **FamilyBoard-Setup-XXXX** på mobilen | Vent 2 minutter etter at Pi-en fikk strøm. Ta ut og sett i strømmen igjen hvis den sto på da WiFi-en forsvant. Selvbygde Pi-er har ikke oppsettsnettet. |

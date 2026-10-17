# Automatisk opplasting fra mobilen (Immich-appen)

Med Immich-appen havner nye bilder fra mobilen automatisk på FamilyBoard-dashboardet.
Det gjelder brukere med **Immich fra FamilyBoard** (se [immich.md](immich.md)).

## Oppsett
1. Installer **Immich** fra App Store (iPhone) eller Google Play (Android).
2. Åpne appen. I feltet for serveradresse skriver du:
   ```
   https://photos.familyboard.cloud
   ```
   (Adressen står også under Profil → 🖥️ Immich i FamilyBoard.)
3. Logg inn med **samme e-post og passord som i FamilyBoard**.
4. Gå til **backup** i appen (sky-ikonet / Account → Backup):
   - Velg hvilke album som skal lastes opp, for eksempel «Kamera» / «Recents»
   - Slå på **bakgrunnsbackup** («Background backup»)
   - Trykk **«Start backup»**

I FamilyBoard finnes den samme guiden under **«📱 Koble mobilen»** på profilsiden
og **«📖 Se mobil-oppsett»** på slutten av veiviseren.

## Tips
- **Partner eller samboer** kan logge inn med samme konto i appen på sin telefon.
- Velg «kun Wi-Fi» hvis du vil spare mobildata.
- På iPhone går bakgrunnsbackup tregere. Åpne appen innimellom for å få opp farten.
- Første backup av et stort bibliotek kan ta lang tid. La telefonen stå på lading og Wi-Fi.
- Bildene vises på dashboardet noen minutter etter opplasting.
- Lagringen teller mot planen din. Se [plans-and-billing.md](../plans-and-billing.md).

## Problemer
- **«Feil passord» i appen:** Bruk FamilyBoard-passordet. Har du byttet passord i FamilyBoard etter at
  Immich ble satt opp, kan Immich fortsatt ha det gamle.
- **Appen finner ikke serveren:** Sjekk at adressen er skrevet nøyaktig, med `https://`.
- **Bildene kommer i appen, men ikke på dashboardet:** Vent noen minutter. Sjekk deretter at
  bildekilden er Immich, og at filtrene ikke utelukker de nye bildene (se [immich.md](immich.md#bildefiltre-immich)).

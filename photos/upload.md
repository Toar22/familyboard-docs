# Laste opp bilder

Brukeren kan laste opp bilder direkte i nettleseren, uten app.

## Hvor
- **Administrasjon → Bildeinnstillinger → «Opplastede bilder» → «⚙️ Innstillinger»** åpner «🖼️ Administrer bilder»
- Brukere med Immich: **Immich → «⚙️ Innstillinger»** har de samme opplastingsknappene

Hvordan man åpner Administrasjon: se [settings.md](../settings.md#åpne-innstillingene).

## Tre måter å laste opp

| Knapp | Bruk når | Detaljer |
|---|---|---|
| **«📁 Last opp noen bilder»** | Noen få utvalgte bilder | Dra og slipp, eller klikk for å velge. JPG, PNG, WebP, GIF, **maks 20 MB per fil**. |
| **«📂 Last opp hele mappe»** | En mappe med undermapper | Viser antall og størrelse før opplasting starter |
| **«📦 Last opp ZIP-fil»** | Mange bilder på én gang (raskest) | ZIP-filen pakkes ut i bakgrunnen. Store filer kan ta litt tid før bildene vises. |

### Hvor havner bildene?
I «Administrer bilder» finnes bryteren **«Opplasting / lagring»**:
- **FamilyBoard**: bildene lagres hos FamilyBoard
- **Immich**: bildene havner i Immich-biblioteket ditt (anbefalt hvis du bruker Immich)

## Administrere opplastede bilder
**«🗑️ Administrer bilder»**:
- Lag mapper (**«+ Ny mappe»**) og dra bilder mellom dem
- Klikk ✓/✗ på en mappe for å ta den med i eller utelate den fra fremvisningen
- Velg flere mapper med Ctrl+klikk → **«Slett valgte»**

**«🗑️ Slett alle opplastede bilder»** sletter alt som er lastet opp via FamilyBoard.
Bilder fra mobilen og ellers i Immich slettes ikke. **Kan ikke angres.**

## Lagringsgrense
Lagringen avhenger av planen (Gratis: 10 GB). Se [plans-and-billing.md](../plans-and-billing.md).

## Feilmeldinger
| Melding | Tiltak |
|---|---|
| «Filen er for stor. Maksimal størrelse er X MB» | Bruk mindre bilder eller pakk dem i ZIP |
| «Ingen bilder funnet i mappen.» | Mappen har ingen støttede bildefiler (JPG, PNG, GIF, WEBP). HEIC fra iPhone kan være et problem. Bruk Immich-appen i stedet. |
| «Ingen bilder ble lastet opp» / «Opplasting feilet» | Sjekk nettverket og prøv igjen. Prøv mindre bunker. |
| «📁 Opplastede bilder aktivert - ingen bilder funnet …» | Kilden er valgt, men det er ingenting lastet opp ennå |

> FamilyBoard er **ikke** en backup-løsning. Behold alltid originalene.

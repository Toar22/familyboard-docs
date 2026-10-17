# Opprette konto og logge inn

FamilyBoard-kontoer opprettes på **https://familyboard.cloud**.

## Opprette konto

1. Gå til familyboard.cloud og velg **«Ny bruker? Opprett konto»**.
2. Fyll inn **E-post** og **Passord**.
   - Passordet må være **minst 8 tegn** og inneholde **minst én bokstav og ett tall**.
3. Trykk **«Opprett konto»**.
4. Du får meldingen *«Konto opprettet! Sjekk e-posten din for å bekrefte kontoen.»*
5. Åpne e-posten fra FamilyBoard og klikk på bekreftelseslenken.
6. Logg inn. Du sendes automatisk til oppsettsveiviseren — se [wizard.md](wizard.md).

> **Viktig å vite:** Passordet du velger her blir også passordet til din personlige
> Immich-bildelagring (hvis du bruker den som FamilyBoard setter opp for deg).
> Se [../photos/immich.md](../photos/immich.md).

## Vanlige problemer

| Melding / situasjon | Hva det betyr | Hva brukeren skal gjøre |
|---|---|---|
| «Passord må være minst 8 tegn langt» | For kort passord | Velg et lengre passord |
| «Passord må inneholde minst 1 bokstav» / «… minst 1 tall» | Passordet mangler bokstav eller tall | Legg til det som mangler |
| «E-posten er allerede i bruk.» | Det finnes allerede en konto med denne e-posten | Logg inn i stedet, eller bruk **«Glemt passord?»** |
| «E-posten din er ikke bekreftet ennå. Sjekk innboksen din.» | Kontoen er opprettet, men e-posten er ikke bekreftet | Sjekk innboks **og søppelpost**. Det er mulig å be om ny bekreftelseslenke fra innloggingssiden. |
| «Bekreftelseslenken er ugyldig eller utløpt.» | Lenken er gammel eller allerede brukt | Be om ny lenke fra innloggingssiden. Hvis meldingen sier at e-posten allerede er bekreftet, kan brukeren bare logge inn. |
| «Kunne ikke opprette konto. Prøv igjen senere.» | Midlertidig feil hos FamilyBoard | Vent noen minutter og prøv igjen. Vedvarer det: kontakt support. |
| «Bruker-opprettelse er ikke tillatt i Edge mode …» | Brukeren prøver å registrere seg på en Raspberry Pi-installasjon | Kontoen må opprettes på familyboard.cloud først. Deretter logger man inn på Pi-en med samme konto. |

## Glemt passord

Trykk **«Glemt passord?»** på innloggingssiden, skriv inn e-posten og følg lenken
du får tilsendt. Av sikkerhetshensyn sier FamilyBoard alltid
*«Hvis kontoen finnes, vil du motta en e-post»* — også når e-posten ikke er registrert.

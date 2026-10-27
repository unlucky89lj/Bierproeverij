# 🍷 Wijnproeverij

Samen blind wijn proeven met je vrienden: aan het rad draaien voor het thema, een datum en locatie prikken, wijnen scannen of kiezen, de vragenlijst invullen en zien wie het best proeft. Een kopie van de Bierproeverij, maar dan voor wijn.

**Open de app:** https://unlucky89lj.github.io/Bierproeverij/wijn/

## Wat zit erin
- **Home, Proeven, Scannen, Uitslag, Tips, Kaart, Agenda en Wijnen**: zoals in de app op claude.ai.
- **Catalogus** met 865 wijnen uit 28 landen (`catalog.json`), met wijnhuis, streek, druiven, stijl, alcohol, indicatieve prijs en labels.
- **Meerdere proeverijen:** elke groep is een aparte proeverij met een eigen uitslag. Meedoen met een code, de beheerder laat je toe.
- **Op je beginscherm:** open de link in Safari of Chrome en kies *Zet op beginscherm*. Je krijgt het wijnglas-icoon.

## Voorbeeldmodus en database
Zolang `../firebase-config.js` leeg is, draait de app in **voorbeeldmodus**: alles blijft op je eigen apparaat. De wijnapp gebruikt dezelfde Firebase-instellingen als de bierapp, maar eigen verzamelingen (beginnend met `wijn_`), zodat bier en wijn elkaar niet raken. De regels staan in `../firestore.rules`.

## Bestanden
| Bestand | Wat |
|---|---|
| `index.html` | de app |
| `backend.js` | koppeling met de database (of voorbeeldmodus) en het kiezen van een proeverij |
| `catalog.json` | de wijnlijst |
| `i18n.json` | vertalingen (EN, DE, FR, ES) |
| `manifest.webmanifest`, `sw.js`, `icons/` | app-icoon en werken als app op je telefoon |

## Agenda-abonnement
`agenda.ics` is het agenda-abonnement van de groep (https://unlucky89lj.github.io/Bierproeverij/wijn/agenda.ics).
De app zet de volgende proefavond in het document `meta/agenda`; een geplande taak draait
`python3 tools/update_agenda.py <meta-agenda.json>` (vanuit deze map) en pusht het bijgewerkte bestand.

Gemaakt en bijgehouden met Claude.

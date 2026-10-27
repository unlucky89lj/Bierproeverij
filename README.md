# 🍺 Bierproeverij

Samen blind bier proeven met je vrienden: aan het rad draaien voor het thema, een datum en locatie prikken, bieren scannen of kiezen, de vragenlijst invullen en zien wie het best proeft.

**Open de app:** https://unlucky89lj.github.io/Bierproeverij/

🍷 **Ook voor wijn:** de [Wijnproeverij](https://unlucky89lj.github.io/Wijnproeverij/) heeft dezelfde functies (repo [unlucky89lj/Wijnproeverij](https://github.com/unlucky89lj/Wijnproeverij)).

## Wat zit erin
- **Home:** wie mag draaien, categorie, datum, proefwijze (standaard of blind), locatie, ranglijst en *Mijn proeverijen*.
- **Proeven, Scannen, Uitslag, Tips, Kaart, Agenda en Bieren**: zoals in de app op claude.ai.
- **Meerdere proeverijen:** elke groep is een aparte proeverij met een eigen uitslag. Meedoen met een code, de beheerder laat je toe.
- **Op je beginscherm:** open de link in Safari of Chrome en kies *Zet op beginscherm*. Je krijgt het bierpul-icoon.

## Voorbeeldmodus en database
Zolang `firebase-config.js` leeg is, draait de app in **voorbeeldmodus**: alles blijft op je eigen apparaat. Vul je de gegevens van een (gratis) Firebase-project in, dan worden de proeverijen gedeeld en log je in met Google of e-mail. De beveiligingsregels staan in `firestore.rules`.

## Bestanden
| Bestand | Wat |
|---|---|
| `index.html` | de app |
| `backend.js` | koppeling met de database (of voorbeeldmodus) en het kiezen van een proeverij |
| `catalog.json` | de bierlijst |
| `firebase-config.js` | instellingen van de database |
| `firestore.rules` | beveiligingsregels voor de database |
| `manifest.webmanifest`, `sw.js`, `icons/` | app-icoon en werken als app op je telefoon |

Gemaakt en bijgehouden met Claude.

## Agenda-abonnement
`agenda.ics` is het agenda-abonnement van de groep (https://unlucky89lj.github.io/Bierproeverij/agenda.ics).
De app zet de volgende proefavond in het document `meta/agenda`; een geplande taak draait
`python3 tools/update_agenda.py <meta-agenda.json>` en pusht het bijgewerkte bestand.

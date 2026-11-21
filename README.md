# Legater

En enkel, filtrerbar oversikt over norske stipender og legater. Live på GitHub Pages.

- `index.html` – appen (ingen byggesteg, ingen avhengigheter)
- `legater.json` – alle ordningene

## Legge til en ordning

Legg til et objekt i `legater` i `legater.json`:

```json
{
  "id": "unik-id",
  "navn": "Navn på legatet",
  "giver": "Hvem som deler ut",
  "belop": "Beløp eller hva det dekker",
  "beskrivelse": "Kort om hvem som kan søke",
  "frist": { "mnd": 10, "dag": 1 },
  "fristTekst": "1. oktober hvert år",
  "niva": ["bachelor", "master"],
  "fag": ["alle"],
  "sted": ["usa"],
  "type": ["privat"],
  "lenke": "https://..."
}
```

Bruk `"frist": null` når datoen ikke er fast. Gyldige verdier for `niva`, `fag`, `sted` og `type` står under `kategorier` øverst i filen.

Filtrene ligger i URL-en (f.eks. `#niva=master&sted=uk`), så et filtrert utvalg kan bokmerkes eller deles.

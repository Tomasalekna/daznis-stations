# Dažnis – stočių pataisos

Programa Dažnis šį failą (`stations.json`) parsisiunčia paleidžiant ir pritaiko ant Radio-Browser stočių sąrašo. Pakeitimai programoje atsiranda per ~5 min. (reikia iš naujo paleisti programą arba patraukti sąrašą žemyn).

## `stations` – pakeisti arba pridėti stotį

```json
{ "country": "LT", "name": "M-1", "url": "https://stream.m-1.fm/m1/mp3" }
```

- `country` – šalies kodas: `LT`, `DK`, `GB`.
- `name` – stoties pavadinimas. Jei toje šalyje jau yra stotis tokiu pavadinimu (didžiosios raidės, tarpai, brūkšneliai ir lietuviškos raidės nesvarbu), jai pakeičiamas srauto adresas. Jei nėra – stotis pridedama.
- `url` – srauto adresas.
- `logo` (nebūtina) – logotipo paveikslėlio adresas.
- `id` (nebūtina) – Radio-Browser stoties UUID. Nurodyk seną stoties ID, kai stotis dingo iš Radio-Browser, kad žmonių mėgstamiausios ir žadintuvai toliau veiktų.

## `hidden` – paslėpti stotį

Sąrašas pavadinimų arba Radio-Browser UUID: `"hidden": ["M-1 Radio", "Radijo stotis M-1"]`

## Svarbu

Failas turi būti teisingas JSON (kableliai tarp įrašų, jokio kablelio po paskutinio). Jei failas sugadintas, programa jį ignoruoja ir naudoja paskutinę veikusią versiją. Prieš išsaugant patikrink, pvz., https://jsonlint.com

# Labo 2 - reflecties

Verhesen Tristan: (jouw naam)

## 2. Selectors lezen

Welke elementen raakt elke selector? Eén zin per selector.

- a. `header nav ul li a`: alle list items in de nav
- b. `article > p`: alle p tags in de a tags
- c. `.uren li:nth-child(3)`: in de classe uren de derde list item
- d. `h2 ~ p`: alle p tags die op hetzelfde niveau staat als alle h2 tags
- e. `.rassen li:first-child`: in de classe rassen de eerst list item van de li onder ul

## 3. Voorspel, dan kijk

Vul de eerste twee kolommen in vóór je de pagina opent. Trede: herkomst, specificiteit, volgorde of overerving (of iets anders, benoem het).

| vraag | mijn voorspelling (kleur) | beslissende trede | uitkomst in de browser | juist? |
|---|---|---|---|---|
| 1 | groen| specificiteit| groen| juist|
| 2 | blauw| specificiteit| blauw| juist|
| 3 | rood| specificiteit| rood| juist|
| 4 | rood| specificiteit| rood| juist|
| 5 | blauw| specificiteit| blauw| juist|
| 6 | blauw| specificiteit| blauw| juist|
| 7 | rood| specificiteit| rood| juist|
| 8 | rood| specificiteit| blauw| fout|
| 9 | blauw| specificiteit| rood| fout|
| 10 | groen| specificiteit| groen| fout|

Bij welke vraag zat je fout, en wat was de reden? (Alles juist? Welke vraag duurde het langst, en waarom?)
vraag 8,9 fout ik heb ze omgedraait denk ik

## 4. De nabouw

- Welke selector koos je voor de links in de navigatie, en waarom geen class?
nav a omdat het niet nodig was dit was de meest specifieke manier om het te beschrijven
- Welke regel kostte je het meeste tijd, en wat was uiteindelijk de oorzaak?
7,8 de juiste manier van het noteren syntax fouten

## 6. Je site

- Welke drie waarden staan in je tokenblok, en waarom die?
--color-paper
--color-accent
--font-heading
- Wat verandert er in je site als je één token wijzigt?
Als je de waarde van één variabele in :root aanpast (bijvoorbeeld --color-accent van geel naar blauw verandert), veranderen automatisch alle elementen op de hele website die die variabele gebruiken

## Thuis: R2.3 (met AI)

Prompt en onbewerkte output staan in `review/`. Minstens vijf bevindingen, elk met een verwijzing naar de sectie of het foutnummer:

1. Opdracht 4 (Combinatorfout): In regel 4 is main p gebruikt, waardoor alle paragrafen cursief worden. De opgave vroeg om de paragraaf onmiddellijk na elke h2. Dit moet de adjacent sibling combinator h2 + p zijn.

2. Opdracht 8 (Verkeerde scoping bij :focus): In main a:hover, a:focus ontbreekt main bij het tweede deel na de komma. Hierdoor geldt de gele achtergrond bij :focus voor elke link op de hele website (ook in de header en footer) in plaats van enkel links binnen main. Dit hoort main a:hover, main a:focus te zijn.

3. Opdracht 5 & 6 (Ongewenste spatie bij pseudo-class): Bij .uren :nth-child(odd) en .uren :last-child staat een spatie tussen de classnaam en de dubbelepunt. Hierdoor selecteert de browser afstammelingen van kinderen in plaats van direct de lijstitems van .uren. Dit moet .uren > li:nth-child(odd) of .uren li:nth-child(odd) zijn.

4. Opdracht 6 (Dubbele / overbodige declaratie): In regel 6 is background-color: #f1e9dc; onnodig herhaald, terwijl de opdracht uitsluitend vroeg om color: crimson;.

5. Opdracht 3 (Onnodig hoge specificiteit): Bij ul.rassen > li is het specificeren van de tag ul overbodig. .rassen > li is korter, heeft een lagere specificiteit en is daardoor beter herbruikbaar en te onderhouden.

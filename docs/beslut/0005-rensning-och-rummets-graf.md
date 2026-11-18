# 0005: Rensning inför bygget, och rummets graf

**Datum:** 10 november 2026 · **Status:** beslutat (prototyp V16) · **Ersätter delar av:** 0003

## Läge
Prototypen hade vuxit från V8 till V15. Gustav tyckte att den hade blivit rörig och bad om att ta bort "allt som är onödigt, överflödigt eller för svårt att implementera och inte ger något större värde".

## Beslut
**Rummets sida är en graf med två val och filtret Väder:**
- *Luftfuktighet:* procent över tid, med en streckad gräns.
- *Från huset* i rum utan avfuktare, eller *Avfuktaren* (timmar per dygn) i rum med avfuktare.
- *Väder* lägger till uteluften i läget Luftfuktighet, eller skuggar perioder med fuktig uteluft i läget Avfuktaren.

**Borttaget eller framskjutet:**

| Vad | Varför |
|---|---|
| Liter per dygn, tankstorlek, tank eller slang | Kräver kalibrering (A1) och ger lite. Timmar och kostnad räcker. |
| Tapo som uttag | Varje märke är en egen integration. Version 1 har bara Shelly. |
| Att appen själv läser av inställd procent och ser när den ändras | Logik som kan slå fel. Appen frågar i stället en gång. |
| Effekttexter vid händelser ("halverades") | Svårt att räkna fram rättvist med årstiderna. Händelserna syns i grafen. |
| "Uppdaterad 07:40" | Version 1 har uppladdning för hand. Översikten visar ärligt "Data till …" och "Ladda upp ny". |
| Tips om konsulten, "Vinter för vinter", Trend-sidan, separat analyssida | Ingick redan i V11–V14. Gav brus mer än värde. |
| Full inloggning | Ett publikt demoläge plus ett enkelt lösenord för egen data räcker i version 1. |

**Så räknas timmar per dygn:** energin per dygn från uttagets mätare delat med effekten när avfuktaren går, cirka 250 W. Det räcker med en avläsning per dygn, vilket passar Vercels schemalagda jobb, som körs en gång per dygn. När tanken är full drar avfuktaren inget, så den tiden räknas inte.

**Kvar, eftersom det är enkelt och ger värde:**
- fukt från huset (Govee plus SMHI plus en formel)
- status över tid
- risk för rost
- kostnad
- väderfiltret
- perioderna
- tips med källor
- Lägg till avfuktare (procent, uttag och elpris)
- Lägg till händelse (var, vad, när och en anteckning)

## Följder
- A1, A1b, A1c och A1d gäller inte längre. A10 är ändrat.
- Spikarna avgör om appen fungerar på riktigt: Govee-CSV (A5), Shellys energi per dygn (A6) och SMHI-station.

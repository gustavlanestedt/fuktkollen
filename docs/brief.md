# FuktKollen: brief

*Version 1, 10 november 2026. Briefen är en sida och uppdateras när något viktigt ändras.*

## Syfte
**FuktKollen håller koll på om fukten går åt rätt håll, och varför.**

## Problemet
Den som åtgärdar en fuktig källare vet inte om åtgärderna fungerar. Sensorappar visar siffror men inte riktningen. När en avfuktare håller luften på 50 % blir kurvan platt, oavsett om källaren torkar eller inte. Oron finns kvar tills konsulten mäter.

## Det unika
**Avfuktaren håller luften jämn. FuktKollen visar fukten som avfuktaren tar bort, och om den blir mindre.**

1. **Timmar per dygn som avfuktaren går:** smarta uttagets energi per dygn delat med effekten när den går. Det fungerar med tank och slang och kräver ingen kalibrering (beslut 0005).
2. **Vädret räknas bort:** blir det mindre vatten för att källaren torkar, eller för att det är kallt och torrt ute?
3. **Händelserna på samma tidslinje:** rivning, regn, flyttad avfuktare.
4. **Utan avfuktare,** till exempel i garaget, används fukttillskottet i stället: absolut fukt inne minus ute.

**Stegen per rum:** sensor → avfuktare → smart uttag. Appen ger tips om nästa steg när den ser en trend, och hänvisar till en källa. Översikten visar helheten, och det unika visas där det finns data för det.

Ingen konsumentapp gör detta, enligt genomgången 9–10 november. Proffs följer uttorkning på liknande sätt, till exempel med DryLINK. Det kräver bara en avfuktare och ett uttag med energimätning för cirka 250–300 kr, och många källare har redan en avfuktare.

## Användaren
**Version 1: Gustav.** Han har ett hus från 1934 med för hög fukt i källaren. Han river ut trägolv och inklädnad ner till betongen och sätter in en avfuktare. Han har också en MC i ett kallt garage och är ofta borta länge. Han har tre Govee-sensorer och ett Shelly-uttag med energimätning på avfuktaren.
**Två typer av användare:**
- **Den vardagliga,** till exempel en 55-åring utan teknikvana. Hen vill se om det är okej och få veta vad hen ska göra.
- **Den nördiga.** Hen vill ha avfuktare, uttag, väder, detaljer och export.

**Senare:** andra som torkar ut en källare eller krypgrund, eller som har haft en vattenskada.

## Behoven (se [insikter](research/insikter.md))
1. **B1:** se om fukten går åt rätt håll efter en åtgärd. *Kärnan.*
2. **B2:** överblick per plats med färg som visar risk.
3. **B4:** förstå om fukten kommer utifrån, med vädret som jämförelse.
4. **B5:** veta om klimatet är bra för MC:n i garaget.
5. **B6:** läsa mer från en trovärdig källa.

B3, varningar, löses redan av Govee och Shelly.

## Principer
- **Snabbkollen först.** Översikten svarar bara på en fråga: är allt ok? Den ska fungera för mamma, som har låg teknikvana: hon öppnar, ser grönt eller orange och stänger. Allt annat finns ett tryck bort.
- **Lågt golv, högt tak.** Det ska vara enkelt att börja, och tydligt hur man kan anpassa mer. En 55-åring utan teknikvana ska klara starten. Den som är nördig ska kunna lägga till avfuktare, uttag, vädersamband och export.
- **Två nivåer, och varje sak visas en gång.** Översikten: är allt okej? Rummet: analysen är huvudsaken. Procenten står bara som en rad överst, eftersom man redan har sett den på översikten.
- **Tips bara när värdet är dåligt,** och då med en riktig källa. Inga tips som bara gissar, som "dags för konsulten?".
- **Varje skärm gör en sak.** Facktermer som g/m³ och kWh ligger bakom "Visa mer".
- **Tips kommer när de behövs,** inte i början.
- **Tydligt före smart.** Startsidan ska gå att förstå på en sekund.
- **Bara det Govee-appen inte gör.**
- **Färgen visar risk, inte bara procent.**
- **Iakttagelse, inte diagnos.** Appen säger aldrig "torrt", "mögel" eller "du behöver dränera". Beslut tar konsulten.
- **Gratis och utan abonnemang.**
- **Tillgänglig från början.** Färg är aldrig den enda signalen.

## Inte med
Appen ställer ingen diagnos, ersätter inte konsulten, styr inga apparater och säljs inte. Version 1 har inga egna larm och ingen automatisk import.

## Så vet vi att det fungerar (avstämning 7 december)
- **Fortsätt** om startsidan ger bättre överblick än Govee-appen **och** trendvyn visar om källaren går åt rätt håll utan förklaring.
- **Ändra** om bara den ena delen håller.
- **Lägg ner eller byt** om Govee- och Shelly-apparna räcker.

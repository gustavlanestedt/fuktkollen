# Antaganden

*Det som måste vara sant för att FuktKollen ska fungera. De mest riskabla står först.*

| # | Antagande | Test | Status |
|---|---|---|---|
| A1 | Avfuktarens energi per dygn visar hur mycket fukt som kommer in, och går att räkna om till liter. | Jämför 3–4 tömningar av tanken med uttagets kWh. Mät tanken en gång med ett litermått. | Inte längre aktuellt (beslut 0005) |
| A1b | Liter per kWh ändras med temperaturen. En kall källare ger mindre vatten per kWh. | Kalibrera vid olika temperaturer, eller räkna om med Govee-temperaturen. | Inte längre aktuellt (beslut 0005) |
| A1c | En full tank och en tömning syns i uttagets effekt, så kalibreringen kan ske automatiskt. Full tank betyder stopp tills någon tömmer, och det måste kunna skiljas från stoppen vid 50 %. | Titta på effektkurvan runt några tömningar. | Inte längre aktuellt (beslut 0005) |
| A1d | Med slang, alltså utan tank, räcker kWh per dygn jämfört med starten för att se riktningen. Liter går bara att få fram med en engångsmätning i hink. | Jämför kWh-trenden med tömningar medan det fortfarande är tank. | Inte längre aktuellt (beslut 0005) |
| A2 | Vädret, alltså fukten ute och regnet, påverkar källaren så att det syns. | SMHI-spiken plus 4 veckor av egna data. | Ej testat |
| A3 | Färg efter risk ger bättre överblick än siffrorna i Govee-appen. | Prototypen jämförs med Govee-appen, sida vid sida. | Ej testat |
| A4 | Trendvyn går att förstå utan förklaring. | Prototypen visas för Gustav och 1–2 andra i 10 minuter. | Ej testat |
| A5 | Govees CSV-fil har det som behövs: tidsupplösning och alla sensorer. | Första exporten. | Ej testat |
| A6 | Data från Shelly går att få ut, antingen som export eller via API. | Spik när uttaget är uppkopplat. | Ej testat |
| A7 | Om vatten tar sig in via marken växer skillnaden mot ute efter kraftigt regn eller snösmältning, och den ligger kvar. Ingen källa anger hur lång fördröjningen är, så vi letar inom 0–7 dygn. *Ändrad 10 november efter research, se research/fukt-regn-arstider.md.* | Jämför skillnaden mellan inne och ute före och efter regn över 10 mm. Kräver minst 5 kraftiga regn. | Ej testat |
| A8 | I ett rum med avfuktare syns vädret i avfuktarens arbete (kWh per dygn), inte i luften. | Jämför kWh per dygn med uteluftens g/m³ och regnet när Shelly-uttaget har varit igång i 4 veckor. | Ej testat |
| A9 | Govee och SMHI räcker för att mäta skillnaden mot ute. Skillnader över 0,5 g/m³ är verkliga. | Ställ alla tre sensorer bredvid varandra ett dygn innan de sätts upp. Om det går: en sensor ute under tak en vecka jämfört med SMHI. | Ej testat |
| A10 | Timmar per dygn går att räkna fram som uttagets energi per dygn delat med effekten när avfuktaren går, cirka 250 W. Det fungerar med både tank och slang. | Läs av effekten när den går, och jämför energin per dygn med hur länge den faktiskt går under en dag. | Ej testat |

# Fukt i källaren: regn, uteluft och årstider

*Research 10 november 2026. Underlaget för hur FuktKollen visar och tolkar fukten. Siffror i hakparentes, till exempel [1], hänvisar till källorna längst ner. Det som är vår egen beräkning eller bedömning står som det.*

## Svaret i korthet

1. **Fukten i källaren stiger när det regnar. Oftast är det helt normalt.** Regnet gör uteluften fuktig, och källarluften följer uteluften. I en amerikansk mätstudie följde källarluften uteluften med 6–12 timmars fördröjning, och uteluften förklarade ungefär 70 % av hur fukten i källaren varierade [5]. Inne och ute stiger alltså nästan samtidigt, och **skillnaden mellan dem ändras inte**.
2. **Det som inte är normalt är om skillnaden mot ute växer efter regn och ligger kvar.** Då kan vatten ta sig in via marken: ytvatten som rinner mot huset, stuprör, dålig lutning, en igensatt dränering eller högt grundvatten [1][8]. Den vägen är långsam, och skador kan ta många år att synas [1].
3. **Ingen källa anger hur många dygn det tar innan regnvatten syns i källarluften.** "1–3 dygn" i prototypen är vårt eget antagande (A7). Det beror på jordart, dränering och grundvatten.
4. **Sommaren är den fuktigaste tiden i en källare, och det beror inte på regnet.** Varm uteluft kyls av den kalla marken och väggarna, och då stiger den relativa fuktigheten [2]. I krypgrunder finns risk för mögel regelbundet från april/maj till augusti/september, och risken är störst kring månadsskiftet juni/juli [3]. Värst är en lång kall vår följd av en varm och fuktig sommar [3][4]. Det sämsta året kan ha fyra gånger så hög risk som det bästa [3].
5. **Vinterhalvåret visar bäst om källaren har en egen fuktkälla.** Uteluften är torr då, så extra vatten inne syns tydligt som en skillnad i gram per m³.
6. **Grundvattnet i västra Götaland är högst på vintern och våren och lägst på sensommaren** [7]. Det stiger igen med höstregnen.
7. **På hösten släpper betong och trä fukt som de tog upp under sommaren** [6]. Det kan ge förhöjd fukt i september–oktober utan att något har gått sönder.

## 1. Två vägar in

| | Via luften | Via marken och vattnet |
|---|---|---|
| **Vad händer** | Fuktig uteluft kommer in genom ventilation och otätheter. | Vatten i marken sugs in i betongen och vidare in i rummet. Det kan vara regn, snösmältning, stuprör, ytvatten eller grundvatten [1][6][8]. |
| **Hur fort** | Timmar. I studien 6–12 timmar [5]. | Långsamt. Boverket kallar det "en långsam process" [1]. Exakt hur långsamt vet vi inte. |
| **Hur mycket** | Begränsat av hur fuktig uteluften är. | Kan vara mycket större. En simulering av en betongvägg gav ungefär 11 kg vatten per m² och år genom kapillärsugning, mot ungefär 1 kg genom ånga [10]. |
| **Så syns det i datan** | Inne och ute stiger och sjunker samtidigt. Skillnaden ligger still. | Skillnaden mot ute växer efter regn eller snösmältning och ligger kvar i flera dygn. Den syns tydligast på vinterhalvåret. |
| **Normalt?** | Ja. | Värt att undersöka, och något för fuktkonsulten. |

**Skyfall är en tredje sak.** Om vatten står på golvet efter ett skyfall har det oftast trängt upp genom golvbrunnen, eftersom dagvattnet har slagit bakåt, eller kommit in genom källartrappan eller fönstren [8]. Det fångar inte en fuktsensor i luften, och appen ska inte försöka ställa den diagnosen.

## 2. Normalt eller varningstecken

**Normalt:**
- Fukten inne stiger samma dag som ett regnväder, ungefär lika mycket som ute.
- Ett kallt källarrum har högre relativ fuktighet på sommaren än på vintern.
- Fukten är förhöjd i september–oktober, när materialen släpper sommarens fukt [6].
- Skillnaden mot ute är liten och ligger inom mätfelet (se avsnitt 5).

**Varningstecken:**
- Skillnaden mot ute växer efter kraftigt regn eller snösmältning och ligger kvar. Det ska ha hänt **flera gånger**, inte bara en.
- Skillnaden mot ute är tydligt över noll under hela vinterhalvåret. En vanlig tumregel bland praktiker är att mer än 1 g/m³ över tid tyder på en egen fuktkälla. Vi har inte hittat den regeln i någon primärkälla.
- Synliga tecken: fuktfläckar, saltutfällningar, flagnande färg eller puts, rost på installationer och lukt [1].
- Relativ fuktighet över ungefär 75 % under **lång tid** (se avsnitt 4).

## 3. Ett år i källaren

| | Vinter (dec–feb) | Vår (mar–maj) | Sommar (jun–aug) | Höst (sep–nov) |
|---|---|---|---|---|
| **Uteluften** | Lite vatten i luften, fast den relativa fuktigheten ute är hög [12]. | Stiger. | Mest vatten i luften. | Sjunker, men hösten har ofta mycket vattenånga och dimma [12]. |
| **Källaren utan egen fuktkälla** | Låg relativ fuktighet. | Stiger. | Högst. Risken för mögel är störst kring juni/juli [3]. | Sjunker långsamt. Materialen släpper fukt [6]. |
| **Grundvattnet** [7] | Högt. | Högt. | Sjunker och är lägst på sensommaren. | Stiger med höstregnen. |
| **Det betyder för appen** | Bäst tid att se en egen fuktkälla. | En kall vår gör att källaren är kall när sommarluften kommer [3]. | Hög fukt är vanlig men riskabel. Avfuktaren gör mest nytta nu. | Förhöjd fukt kan vara normal. |

**Räkneexempel (vår egen beräkning med Magnus formel och typiska värden, inte mätdata):**

| Uteluft | Vatten i luften | Relativ fuktighet i en källare som håller 10 °C | 12 °C | 14 °C |
|---|---|---|---|---|
| Januari, −1 °C och 88 % | 4,0 g/m³ | 42 % | 37 % | 33 % |
| April, 6 °C och 75 % | 5,4 g/m³ | 58 % | 51 % | 45 % |
| Juli, 17 °C och 72 % | 10,4 g/m³ | över 100 %, alltså kondens | 98 % | 86 % |
| Oktober, 8 °C och 85 % | 7,0 g/m³ | 75 % | 66 % | 58 % |

Samma uteluft ger alltså helt olika relativ fuktighet beroende på hur kall källaren är. Det är därför sommaren är farlig, och därför gram per m³ är rätt mått för att jämföra inne och ute.

**En tumregel som är bra att kunna:** vid 10 °C motsvarar 1 g/m³ ungefär 10 procentenheter relativ fuktighet. Vid 14 °C är det ungefär 8. En skillnad på "+1 g" är alltså mycket.

## 4. Mögel: både nivå och tid

- I Fuktcentrums mögelmodell slutar mögel att växa på trä när den relativa fuktigheten är under ungefär 75 %, och det kan till och med gå tillbaka. Över 75 % byggs en "dos" upp över tid. En kort stund över gränsen betyder lite. En lång period betyder mycket [9].
- Gränsen beror på material, temperatur och hur länge fukten varar [13]. 75 % är en förenkling.
- **För appen:** status ska bygga på hur länge rummet har legat över gränsen, inte på ett enskilt värde. Prototypens "Över 70 % i tre veckor" är rätt mönster.

## 5. Hur noggrant kan vi mäta?

- Govee H5179 mäter fukt på ±3 % RF och temperatur på ±0,3 °C [11]. Vid 10 °C är 3 % RF ungefär 0,3 g/m³.
- Uteluften kommer från en SMHI-station, inte från Gustavs tomt. Den kan skilja lite.
- **Vår bedömning:** skillnader under ungefär 0,5 g/m³ ska appen inte tolka. Den säger "som ute".
- **Gör så här innan sensorerna sätts upp:** låt alla tre stå bredvid varandra ett dygn. Spara hur mycket de skiljer sig, och räkna bort det.

## 6. Vad vi inte vet

- **Hur lång fördröjningen är via marken.** Ingen källa anger dygn. Vi får mäta i Gustavs källare.
- **Om studien med 6–12 timmar gäller svenska källare.** Den gjordes på tre amerikanska hus i en radonstudie [5].
- **Tumreglerna för skillnaden mot ute,** alltså "under 0,3 g är brus", "över 1 g över tid är en egen källa" och "mät oktober–mars". De kommer från praktiker. Folkhälsomyndighetens allmänna råd (FoHMFS 2014:14), som brukar nämnas, gick inte att hämta.
- **Räkneexemplen** bygger på typiska värden som vi har valt själva.

## 7. Vad det betyder för FuktKollen

**R1. Två frågor, två mått.**
- *Är det okej nu?* Relativ fuktighet i %, eftersom den visar risken för mögel. Den används på översikten och i statusfärgen.
- *Varifrån kommer fukten?* Skillnaden mot ute i g/m³. Den används i grafen och i kortet "Vädret och fukten".

**R2. Jämför aldrig vinter med sommar.** "Bättre" och "sämre" jämför antingen samma period förra året ("Jämfört med förra hösten") eller skillnaden mot ute, som tar bort vädret.

**R3. Sommarfukt sägs som vanlig men riskabel.** Det ska inte låta som ett larm om en skada. Förslag: "Sommarfukt. Vanligt i källare, när varm luft kyls av. Avfuktaren gör mest nytta nu."

**R4. Ingen tolkning av ett enskilt regn.** Kortet "Regn och fukten" säger något först efter flera kraftiga regn, förslagsvis minst fem. Snösmältning räknas också [6]. Fönstret blir 0–7 dygn i stället för 1–3, tills vi vet mer. Texten är alltid "iakttagelse, inte diagnos".

**R5. I ett rum med avfuktare syns vädret i avfuktarens arbete.** Avfuktaren håller luften jämn. Där jämför appen avfuktarens kWh per dygn med regnet och med uteluftens g/m³, inte med luften inne.

**R6. Vinterhalvåret är facit för en egen fuktkälla.** Grafen kan markera oktober–mars som "bäst att bedöma". Ett kort förklarar varför.

**R7. Mätfelet syns.** I läget "Skillnad" visas ett ljust band kring noll som heter "som ute". Värden inom bandet tolkas inte.

**R8. Status bygger på tid.** Gränserna (70 och 75 %) blir ett eget beslut, 0004, med tid över gränsen inbyggd.

**R9. Inga påhittade normalvärden.** Vi har inga data från andra hus, så appen visar inget band för "normalt för årstiden". Uteluften är referensen.

**Ändringar i prototypen:**
- **Orörda rummet:** "Fukten kommer troligen inifrån" kan läsas som tvätt eller duschar. Byt till "från marken eller väggarna".
- **Grafen, läget "Skillnad":** lägg till bandet "som ute" och en knapp för "Samma tid förra året".
- **Kortet "Regn och fukten":** byt "1–3 dygn" till "inom en vecka", och visa hur många regn analysen bygger på.
- **Rum utan avfuktare på sommaren:** status orange med R3-texten, inte en varning.

## Källor

1. Boverket: [Risker med fuktinträngning från mark till källarvägg](https://www.boverket.se/sv/byggande/forebygg-fel-brister-skador/risker-byggande/risker-fuktskador/fuktrisker-for-grund/fuktrisker-med-kallare/risk-med-fuktintrangning-kallarvagg/)
2. Boverket: [Risker med fukt från uteluft i krypgrund](https://www.boverket.se/sv/byggande/forebygg-fel-brister-skador/risker-byggande/risker-fuktskador/fuktrisker-for-grund/krypgrund/risk-med-fukt-fran-uteluft-i-krypgrund/)
3. Elmroth m.fl.: [Går det att bygga fuktsäkra krypgrunder?](https://www.fuktcentrum.lth.se/fileadmin/fuktcentrum/Publikationer/Bygg-Teknik/5_02_20.pdf), Bygg & teknik 5/02
4. Sikander: [Uppföljning av modifierad, uteluftsventilerad krypgrund](https://www.fuktcentrum.lth.se/fileadmin/fuktcentrum/Publikationer/Bygg-Teknik/8_04_36.pdf), Bygg & teknik 8/04
5. US EPA: [Moisture study, analysis](https://19january2021snapshot.epa.gov/sites/static/files/2014-08/documents/moisturestudy_analysis.pdf)
6. CMHC: [Moisture Problems](https://assets.cmhc-schl.gc.ca/sf/project/archive/research/ca1_mh_87m57.pdf), 1987
7. SGU: [Grundvattennivåns tidsmässiga variationer i morän](https://www.sgu.se/globalassets/produkter/publikationer/tidigare/grundvattennivans-tidsmassiga-variationer-i-moran-och-jamforelser-med-klimatscenarier.pdf)
8. Alingsås kommun: [Källaröversvämning](https://www.alingsas.se/wp-content/uploads/2023/11/kallaroversvamning-JS_SK.pdf)
9. Nilsson: [Mögelpåväxt under varierande fukt- och temperaturförhållanden](https://www.fuktcentrum.lth.se/fileadmin/fuktcentrum/PDF-filer/INFOdagar/Infodag_Lund/2012/Infodag_2012/Moegelpaavaext_under_varierande_fukt-_och_temperaturfoerhaallanden_Lars-OlofNilsson.pdf), Fuktcentrum 2012
10. Ueno: [Capillary Moisture Transport and Foundation Implications](https://buildingscience.com/sites/default/files/2009-01-24-Capillary_Moisture_Transport.pdf), Building Science Corporation 2009
11. Govee: [Wi-Fi Thermo-Hygrometer H5179](https://eu.govee.com/collections/featured-products/products/wi-fi-temperature-humidity-sensor)
12. SMHI: [Relativ fuktighet under året och dygnet](https://www.smhi.se/kunskapsbanken/meteorologi/luftfuktighet/relativ-fuktighet-under-aret-och-dygnet)
13. Lunds universitet: [avhandling om mögel och fukt](https://lup.lub.lu.se/record/4406856)

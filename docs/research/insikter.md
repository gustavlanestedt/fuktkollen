# Insikter

*Senast uppdaterad 10 november 2026. Källor: [intervju med Gustav](2026-11-10-intervju-gustav.md) och marknadsgenomgången från 9 november.*

## Behoven

Behoven skrivs som "När … vill jag … så att …". Kolumnen "Löst av Govee-appen?" visar vad användaren redan får av sensorerna han har köpt.

| # | Behov | Styrka | Löst av Govee-appen? |
|---|---|---|---|
| **B1** | **När jag har gjort en åtgärd**, till exempel rivit eller satt in en avfuktare, **vill jag se om fukten går åt rätt håll över tid, så att oron minskar och jag vet när det är dags att ringa konsulten.** | Starkast. Nämns i svar 1, 2 och 3. | **Nej.** Avfuktaren håller luften på 50 %, så kurvan blir platt. Det som visar uttorkningen är hur hårt avfuktaren arbetar, och det syns bara i Shelly-appen, utan koppling till luften eller vädret. |
| **B2** | När jag öppnar appen vill jag **direkt se läget för varje plats i färg**, så att jag på en sekund vet om allt är okej. | Stark (svar 6) | **Delvis.** Siffrorna finns, men färgen visar inte risk. 75 % betyder olika saker vid 4 °C och vid 18 °C, och efter en timme eller efter en vecka. |
| **B3** | När jag är borta vill jag **få en varning om fukten ökar rejält**, så att jag kan agera eller be någon göra det. | Medel (svar 3) | **Ja.** Govee har larm vid gränsvärden, och Shelly kan larma när avfuktaren stannar. |
| **B4** | När fukten är hög vill jag **förstå om den kommer utifrån**, så att jag och konsulten kan avgöra om dränering behövs. | Stark men osäker (svar 2) | **Nej.** Ingen app jämför källarens fukt med regnet och fukten ute över tid. |
| **B5** | När MC:n står i garaget över vintern vill jag **veta om klimatet är bra för den**, så att den inte tar skada. | Medel (svar 5) | **Delvis.** Siffran finns, men inte vad den betyder för en MC. |
| **B6** | När jag ser ett värde vill jag **kunna läsa mer från en trovärdig källa**, så att jag förstår vad det betyder. | Medel (svar 6) | **Nej.** |

## Vad som får användaren att sluta (svar 7), och vad det betyder för designen

| Han slutar om … | Princip |
|---|---|
| den är otydlig | **Tydligt före smart.** Startsidan ska gå att förstå på en sekund. |
| den inte ger så mycket | **Bygg bara det Govee-appen inte redan gör.** Det är B1, B4 och färgen som visar risk. |
| den kostar mycket | **Gratis.** Inga betaltjänster som kräver abonnemang. |
| en konkurrent är mer användarvänlig och lika nyttig | **Jämför alltid med Govee-appen.** Vid avstämningen ska FuktKollen vinna på överblick och på B1. |

## Djävulens advokat

1. **B2 och B3 är redan lösta av Govee.** Risken är att du bygger en snyggare Govee-app. Startsidan är bara värd att bygga om färgen visar *risk*, alltså luftfuktighet, temperatur och hur länge det har varat, och om alla platser och avfuktaren syns tillsammans. Annars räcker Govee-appen. Bygg inga egna larm i version 1.
2. **I rummet som torkar blir siffran grön hela tiden.** Avfuktaren håller luften på 50 %, så en startsida med bara procent ger en falsk trygghet. Det som visar uttorkningen är avfuktarens arbete per dygn, med vädret bortrensat. Det här är det starkaste skälet till att FuktKollen behövs. Användaren nämnde det inte själv, och därför är det viktigt att prototypen visar det tydligt.
3. **"Blir miljön bättre?" kan luften bara delvis svara på.** Hur fuktig betongen är mäter konsulten. Appen visar trenden och föreslår när det kan vara dags att ringa konsulten, men den avgör aldrig att något är klart.
4. **"Kommer fukten utifrån?"** Appen kan visa att fukten följer regnet, men den kan inte bevisa orsaken. Den gör iakttagelser och föreslår möjliga förklaringar. Beslutet om dränering tar konsulten.
5. **Användaren bad inte om en mening.** AI-funktionen "Läget i klarspråk" kommer alltså från utvecklaren, inte från behovet. Den nedprioriteras. AI kan i stället passa i "Läs mer" (B6), där den förklarar ett värde med hänvisning till en källa. Det avgörs efter prototypen.
6. **Utvecklaren och användaren är samma person.** Du vill gärna att din idé ska vara bra. Motåtgärd: visa prototypen för 1–2 andra i 10 minuter, och jämför ärligt med Govee-appen vid avstämningen.

## Vad det betyder för prototypen

Prototypen ska svara på två frågor:
1. **Startsidan:** ger kort per plats, med färg efter risk och avfuktarens status, bättre överblick än Govee-appen?
2. **Trendvyn för rummet som torkar:** går det att se om det går åt rätt håll, med avfuktarens arbete, vädret och händelserna, utan att någon förklarar?

**Öppna frågor till specen:**
- Vilka gränser ska färgerna ha för källaren (mögelrisk) och för garaget med MC (korrosion och kondens)? Ta fram dem med källor.
- Vilka trovärdiga källor ska "Läs mer" länka till?

## Finns det appar som redan gör B1 och B4? (kontrollerat 10 november)
- **Historik:** ja, i Govee, SwitchBot och Shelly. Användaren vet det redan.
- **Inne jämfört med ute:**
  - **Här och nu, för att avgöra när man ska vädra:** Humidity Window, LüftKit (iOS, bara HomeKit), TFA Bel Air och Bresser VentAir (displayer) och Ventilation Assistant i Home Assistant.
  - **Väderstationer som Ecowitt och Netatmo** visar inne, ute och regn i samma app, men i separata diagram. En användare av Ecowitt bad 2024 om att kunna jämföra sensorer i samma diagram.
  - **Ingen analyserar över veckor och månader** om källaren följer regnet, eller räknar bort vintern.
- **Avfuktarens arbete:**
  - Uttagsapparna (Shelly, Tapo) visar kWh per dygn, men i en egen app utan koppling till fukten eller vädret.
  - I Home Assistant används uttagets effekt för att se om avfuktaren går, är avstängd eller har full tank.
  - Ingen konsumentprodukt använder arbetet per dygn som mått på hur uttorkningen går. Det gör bara proffssystem för uttorkning.
- **Slutsats:** B1 och B4 är luckan och kärnan. Startsidan med överblick (B2) är bara delvis ny. Prototypen ska därför lägga mest vikt på trendvyn.
- **Förbehåll:**
  - Att jag inte har hittat något betyder inte att det inte finns. Humidity Window och LüftKit hittades först i andra sökningen.
  - Home Assistant kan göra allt detta för den som bygger det själv.

## Prototyptest 1 med Gustav, 10 november
**Tre varianter testades:** A, svaret först. B, grafen först. C, platserna först.

**Vad Gustav sa:**
- **Han gillar C.** Överblick per plats, och sedan trycker man på en plats för trender och förklaringar.
- **A var "nice",** men han undrade varför källaren låg överst när den inte var markerad på något sätt.
- **Ingen variant var tydlig direkt.** Liter per dygn förstods inte utan förklaring.
- **Han vill ha fuktprocenten på varje kort.** På platser där man har lagt till en avfuktare ska kortet få en symbol för avfuktaren, och där mäts "det verkliga värdet".
- **Hans önskan:** "Gå mer all in på det unika", men visa också helheten. Garaget har ingen avfuktare, men kanske får det en avfuktare eller en Pax-fläkt senare.

**Slutsatser:**
- **Struktur:** överblicken ger helheten och är dörren in. Det unika syns som en signal på kortet och förklaras fullt på platsens egen sida. Det blir version 2 i prototypen.
- **Ordval:** "fuktkvot" är fel ord. Det betyder fukt i material, till exempel trä, och mäts med stift. Det appen visar är vattnet som avfuktaren tar upp. Formuleringen "Tar upp 2,0 l/dygn" knyter an till tanken, som han redan förstår. Namnet testas vidare.
- **Två unika delar:**
  1. Med avfuktare: vattnet den tar upp, med vädret bortrensat.
  2. Utan avfuktare: fukten inne jämfört med uteluften över tid, till exempel "följer uteluften" eller "fuktigare än ute".

**Är det unikt? Kontroll 10 november:**
- **Konsumentappar till smarta avfuktare** (Midea, Frigidaire, GE och Dreame) visar styrning, luftfuktighet just nu och larm för full tank. Ingen visar vatten per dygn eller hur uttorkningen går.
- **Proffs inom vattenskador** följer uttorkning med avfuktare och fuktmätning. Exempel är DryLINK, kopplat till Phoenix proffsavfuktare, och Xactimate Mitigate.
- **Slutsats:** metoden är beprövad hos proffs, vilket stärker att den håller. Men den finns inte för husägare med en vanlig avfuktare och ett uttag för 250 kr.

**Gustavs idé efter testet: "stegen" per rum (10 november)**
1. **Bara sensor:** procent, färg och jämförelse med uteluften. Om appen ser en trend, till exempel över 70 % i tre veckor och fuktigare än ute, ger den ett tips om att en avfuktare kan hjälpa. Tipset hänvisar till en trovärdig källa, och konsulten avgör.
2. **Avfuktare tillagd:** dagen blir en händelse, och utvecklingen syns från den dagen.
3. **Smart uttag tillagt:** "Tar upp X l/dygn", alltså det unika. Appen tipsar om uttaget i steg 2.
- **Per kort väljer man vad översikten visar:** luftfuktighet eller "tar upp, liter".
- **Varför stegen är bra:** varje rum börjar enkelt och växer med användaren. Appen fungerar med bara en sensor, och det unika kommer när det behövs. Den leder också användaren till den uppställning där appen ger mest.

**Prototyptest 2, samma dag:**
- **"Tar upp 2,0 l/dygn" kändes godtyckligt.** Det fanns ingen referens för vad som är bra. Det finns inte heller något allmänt bra värde, eftersom det beror på rummet och avfuktaren.
  - Lösning: visa riktningen först ("Fukten minskar", på en skala ökar–står still–minskar).
  - Visa sedan något han känner igen: hur ofta tanken blir full, till exempel "var 36:e timme, i början var 16:e".
  - Liter visas bara som detalj.
- **Tipset syntes inte.** Det låg på rummets sida, längst ut till höger på canvasen. Nu syns det också som en banner på översikten.

**Prototyptest 3, samma dag:**
- **Många avfuktare töms med slang,** och då finns ingen tank att jämföra med.
  - Lösning: när man lägger till avfuktaren väljer man tank eller slang.
  - Med slang visar appen hur mycket avfuktaren jobbar, i kWh jämfört med starten.
  - Riktningen kräver inga liter alls. Liter är bara en översättning som gör siffran lättare att förstå.
- **Gustav vill se vad avfuktaren kostar:** kWh gånger elpriset. Det är lätt att bygga och motiverar, eftersom kostnaden sjunker när mindre fukt kommer in.
  - Version 1 använder ett fast elpris som man fyller i själv.
  - Senare kan spotpriset för SE3 hämtas automatiskt.

**Gustavs princip efter testerna (10 november):**
> Appen ska vara väldigt enkel, snygg och kul att använda. Det ska vara lätt för en 55-åring utan mycket teknikvana, men den ska gå att anpassa för nördar också. Det är viktigt att den är enkel att starta med och har tydliga vägar till mer.

- **Det heter "lågt golv, högt tak".** Begreppet kommer från Seymour Papert och Mitchel Resnick. Stegen per rum är vägen uppåt.
- **Prototypen bryter mot principen här:**
  - Garagesidan visar gram per m³ direkt.
  - Torkrummets sida är lång.
  - Detaljerna ska ligga bakom "Visa mer".
- **Testa med en riktig vardagsanvändare:** en 55-åring utan teknikvana, i 10 minuter, med tre uppgifter.

**Designkritik från Gustav av översikten i version 2 (10 november):**
- **Lite kontrast,** allt ser likadant ut, och det framgår inte vad som är viktigt.
- **SMHI-kortet ser ut som en plats.** Man kan tro att det sitter en sensor där.
- **Han vill ha tydligare rubriker** för var platserna är.

**Version 3 av översikten:**
- **Rubriken "Mitt hus"** överst.
- **Vädret som en smal blå remsa** märkt SMHI, inte som ett kort.
- **Tipset som en orange ruta,** "1 sak att titta på".
- **Platserna grupperade** under rubrikerna Källaren och Garaget.
- **Kort i full bredd** med ram, namn i fetstil, stort värde och en pil som visar att man kan trycka.
- **Fyllda statusmärken** i grönt och orange med vit text.
- **Mörkare text** för bättre kontrast.
- **Händelsen** flyttad till fliken Händelser.

**Gustavs beslut om översikten, 10 november: snabbkollen**
> Mamma, som har låg teknikvana, ska kunna öppna appen, snabbt se procenten för varje del och stänga den igen. Inget rörigt. Det viktiga är: är allt ok, är allt grönt, är något rött?

**Version 5 av översikten:**
- **Ett svar överst:** "Allt ser bra ut", eller "2 platser att hålla koll på".
- **Ett stort kort per plats** med namn, en stor procentsiffra, en temperatur och ett statusmärke med ikon och ord (Bra, Förhöjd eller Hög).
- **Huset, vädret, tipsen och menyn är borttagna** från översikten.
- **Platser som behöver uppmärksamhet ligger först.**
- **1–3 platser:** korten ligger under varandra. **2 platser:** korten blir större. **4 eller fler:** två kolumner.
- **Det unika och vädret** visas på platsens egen sida.
- **Status för rum med avfuktare** bygger på trenden ("rätt håll"), inte bara på procenten. Annars ger den falsk trygghet.

**Version 6 av översikten, 10 november:**
- **Gustav om version 4 och 5:** korten i version 4 var mycket snyggare än i version 5, och stapeldiagrammet på torkrummet var både snyggt och tydligt.
- **Det oklara:** "6 °C" bredvid "Förhöjd" gick inte att tolka. Är det temperaturen inne eller ute?
- **Version 6:**
  - Korten från version 4 i samma rutnät, med det höga torkrummet och staplarna från start till nu.
  - Svaret från version 5 överst ("2 platser att hålla koll på").
  - Huset, vädret, listan "Att titta på" och menyn är borttagna.
  - Temperaturen står på en egen rad med termometerikon: "12 °C i rummet" och "6 °C i garaget".

**Version 7, 10 november:** Gustav tyckte att version 4 fortfarande var snyggast. Han nämnde listan "Att titta på" och helheten. Version 7 är därför version 4 utan huset.
- **Status överst:** en lugn rad under "Mitt hus" med en prick och "2 platser behöver koll", i stället för en tung färgad ruta.
- **Vädret** är ett litet märke uppe till höger, "Ute 2°", så att det inte förväxlas med en plats.
- **Korten från version 4 utan temperatur.** Temperaturen finns på platsens sida, så den inte skapar förvirring.
- **Listan "Att titta på"** har en rad per plats som behöver koll.
- **Menyn flyter** och har en svart plusknapp.
- **Detaljerna:** halo runt statusprickarna, 26 px rundning, 18 px luft i korten och en svag skugga.

**Version 8, 10 november:** Gustav sa: "Utgå från version 7, med en logga högst upp och en banner." Version 8 har loggan i toppen och en banner som visar statusen, där färgen följer läget. Under den ligger korten och listan från version 7.
- **Samma dag:** bannern togs bort, eftersom den visade samma sak som "Att titta på". Nu är ordningen: logga, "Mitt hus" med tiden för senaste uppdatering, korten och sedan "Att titta på".

**Vädret, 10 november:** Gustav frågade var vädret syns. Varje platssida har nu kortet "Vädret och fukten", med två rader och en tolkning (se design/riktning.md). Det är där det unika med vädret syns, alltså svaret på "kommer fukten utifrån?" och underlaget för frågan om dränering.

## Granskning av V8 och V9 mot syftet (10 november)
Alla sidor är kontrollerade mot briefen ("om fukten går åt rätt håll, och varför") och mot reglerna i `fukt-regn-arstider.md`.

**Det som fungerar:** översikten är en snabbkoll. Torkrummet visar det unika: mindre vatten, tanken och kostnaden. Trend-sidan visar hur det har gått över flera år. Stegen sensor → avfuktare → uttag finns.

**Det som är fel, viktigast först:**
1. **Torkrummets väderkort** säger "Fukten inifrån har minskat, +3,2 → +0,7 g", men avfuktaren går. Det som syns är avfuktaren, inte huset. Kortet länkar dessutom till den gamla V8-grafen.
2. **Rum utan avfuktare svarar inte på B1.** De visar bara procent och ett tips. Varje rumssida bör ha samma ordning: Nu → Går det åt rätt håll? → Varför → Nästa steg. Bara måttet skiljer sig.
3. **Flera ord för samma sak:** "Över uteluften", "Fukten inifrån", "fukttillskott" och "Fukt från huset". Dessutom finns g/m³ kvar på sidorna för orörda rummet och garaget. Beslut: det heter "fukt från huset" och visas i procent.
4. **Garaget är orange "Förhöjd",** fast fukten kommer från uteluften. Det som är riskabelt är klimatet för MC:n (B5). Gränsen för MC:n saknas.
5. **Statusen bygger på procent just nu,** inte på tid över gränsen eller på årstiden (R3, R8). Gränserna saknar källor (beslut 0004).
6. **Liter är tillbaka på Trend-sidan,** fast test 1 visade att liter kändes godtyckligt.
7. **Garaget visar tipset "Avfuktare eller fläkt här?"** utan att appen har sett någon trend.
8. **Döda länkar och platshållare:** Torkrummet länkar till V8-grafen, och orörda rummet och garaget länkar till "#". V9-grafen länkas inte. Platshållarna [TROVÄRDIG KÄLLA] och [GRÄNS FÖR MC] står kvar.
9. **Tre olika tidslinjer i demon:** översikten är två månader in, V9-grafen stänger av avfuktaren och Trend-sidan är tre år in.

**Saknas, men är med i planen för version 1:** att lägga in en händelse, import av Govee- och Shelly-data, och att välja ort för SMHI.

**När en avfuktare läggs till byter rummet mått.** Händelsen delar grafen i två rader med samma tidsaxel:
- Före: fukt från huset, som en linje.
- Efter: vattnet som avfuktaren tar bort, som staplar.

Utan uttag blir den nedre raden tom, och appen förklarar varför. Det är skälet till steget "smart uttag".

## Fynd från Gustavs egen genomgång av V16 (11 november)
- **Plus-knappen på översikten** tolkades som "lägg till ett nytt rum", men den ledde till "Lägg till händelse". **Åtgärd:** plus öppnar nu en meny med Nytt rum, Händelse och Avfuktare. Sidan Nytt rum är ny: namn, sensor och var rummet ligger. **Lärdom:** en ikon utan text kan betyda olika saker för olika personer. Testa samma sak på mamma (uppgift 6).
- **Spara sparar ingenting**, eftersom prototypen bara är klickbar. Det är väntat och inget fel, men det ska sägas innan testet.

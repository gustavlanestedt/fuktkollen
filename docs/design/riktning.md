# Visuell riktning

*10 november 2026. Bygger på tre skärmdumpar som Gustav tycker är snygga: två konceptappar för bilar och en inställningsskärm för en luftrenare. Bilderna ligger inte i repot, eftersom det är andras verk. Här står bara de drag vi tar efter.*

## Dragen
- **Lugn, ljus bakgrund:** varmt ljusgrå (#F2F2F0) med vita kort, stora rundade hörn (22–24 px), ingen ram och knappt någon skugga.
- **Nästan svartvitt.** Färg används bara som signal: en liten orange prick för "titta här" och grönt för "rätt håll". Färg är aldrig den enda signalen, så det står alltid text bredvid.
- **Stora, lätta siffror:** värdet är stort i normal vikt, enheten är liten och grå, och etiketten är liten med en ikon ovanför.
- *(Struket)* **Ett blickfång överst:** bilen i förebilderna motsvaras av huset i genomskärning, med prickar på varje plats. Prickarna visar också var platserna sitter.
- **Bento-rutnät:** ett högt kort för huvudplatsen och två mindre bredvid.
- **Lista under rubriken "Att titta på"** med en siffra som visar antal: ikonruta, rubrik, en rad text och en prick.
- **Flytande meny som en pill,** och en svart rund knapp för att lägga till.
- **Typsnitt:** Outfit, ett geometriskt sans-serif-typsnitt.

## Designtokens för appen, utkast
| Token | Värde |
|---|---|
| bakgrund | #F2F2F0 |
| kort | #FFFFFF |
| text | #111111 |
| text-dämpad | #5F5F5C |
| signal-bra | #2F7D46 |
| signal-titta | #D97706 (prick), #9A4A06 (text) |
| radie-kort | 24px |
| typsnitt | Outfit 300–600 |

## Kontrollera
- **Kontrast:** dämpad text har minst 4,5:1 mot både vitt och bakgrunden.
- **Storlek:** knappar och tryckytor är minst 44 px.
- **Vardagsanvändaren:** det lugna formspråket får inte göra det otydligt för 55-åringen. Testa.

## Husbilden (struken 10 november)
*Struken från översikten. Den gjorde snabbkollen otydligare. Idén om zoner kan komma tillbaka senare som ett val för den nördiga användaren.*

**Tidigare tankar:**
- **Prickarna går att trycka på** och leder till platsens sida. Färgen följer status. Korten under har samma länkar, så bilden är ett komplement och inget krav. Det gör den tillgänglig för den som använder tangentbord eller skärmläsare.
- **Version 1:** en fast mall med zonerna för Gustavs hus: två rum i källaren och ett garage.
- **Senare, lågt golv:** "Var sitter sensorn?" Man väljer en zon, till exempel krypgrund, källare, bottenvåning, övervåning, vind, garage eller ute. Huset ritas med de zoner som finns, och pricken hamnar rätt.
- **Senare, högt tak:** man drar prickarna själv, eller laddar upp en egen planritning.

## Grunden för översikten (beslut 10 november)
Version 7 är grunden, och version 8 lägger till logga och banner.
- **Loggan, första skissen:** en svart rundad ruta med en vit droppe och en bock i, "koll på fukten". Ordmärket är "Fukt" i 600 och "Kollen" i 300, i Outfit.
- **Bannern (struken samma dag):** den visade samma sak som listan "Att titta på", och därför togs den bort. Statusen finns i listan och i prickarna på korten. När allt är bra visar listan "Allt ser bra ut ✓" i stället.
- *Tidigare idé om bannern:* högst upp, och den bär statusen.
  - Färgen följer läget, platt och utan gradient: ljust orange (#FCEBD9) när något behöver koll, och ljust grön när allt är bra.
  - Den stora rubriken svarar på frågan: "2 platser behöver koll" eller "Allt ser bra ut".
  - En rad prickar visar en prick per plats.
  - En stor, ljus droppe i hörnet är bara dekoration.

## Husets namn
- **Rubriken på översikten är husets namn,** och användaren väljer det själv, till exempel en gatuadress, "Sommarstugan" eller "Mammas hus". Det förbereder också för flera hus senare.
- **Den riktiga adressen finns bara i Gustavs privata prototyp och hans egen inloggade data.** Den finns aldrig i repot, i det publika demoläget, i skärmdumpar till portfolion eller i case studyn. Demot använder ett påhittat namn, till exempel "Exempelvägen 1".

## Platsernas sidor i V8-stilen (10 november)
Samma mönster på alla sidor:
- **Överst:** en rund tillbakaknapp, sidans namn i 34 px och en underrad med till exempel "Källaren · avfuktare på 50 %".
- **Första kortet:** svaret, alltså status med prick och ord och en stor siffra.
- **Sedan:** det man kan göra, med tips och stegen, och en svart knapp i pillform.
- **"Visa mer":** de nördiga detaljerna, som kurvor, g/m³, liter och inställningar.
- **Skärmen scrollar inuti telefonramen**, som i en riktig app.

## Kortet "Vädret och fukten" (10 november)
Varje plats har samma kort, direkt efter svaret, märkt SMHI. Det svarar på behov B4: kommer fukten utifrån? Översikten visar inget om vädret utom "Ute 2°", eftersom den ska vara en snabbkoll.

| Plats | Rad 1 | Rad 2 | Tolkning (iakttagelse, inte diagnos) |
|---|---|---|---|
| **Utan avfuktare** | Jämfört med uteluften: "Följer uteluften", "Fuktigare än ute" eller "Torrare än ute" | Efter kraftigt regn: "Stiger samma dag", "Ökar efter 1–2 dygn" eller "Ingen tydlig ökning" | **Följer uteluften:** fukten kommer troligen utifrån med luften. **Fuktigare och inte påverkad av regn:** fukten kommer troligen inifrån. **Ökar efter regn:** visa konsulten. |
| **Med avfuktare** | Med vädret borträknat: "Minskar ändå", "Står still" eller "Ökar" | Efter kraftigt regn: "Mer vatten 1–2 dygn" eller "Ingen skillnad" | **Mer vatten efter regn:** vatten kan ta sig in utifrån. Visa konsulten, som bedömer om dränering behövs. |

## Årsvyn "Ett år i källaren" (10 november, ersatt samma dag)
*Ersatt av en graf per kort, med förhandsvisning och helskärm. Se nedan.*
- **Ett rum utan avfuktare:** två linjer i samma diagram, källaren (blå, heldragen) och ute (orange, streckad), båda i **gram vatten per m³**. Det är samma enhet och samma axel, och det är det enda ärliga sättet att lägga dem i ett diagram.
- **Ett rum med avfuktare:** liter per vecka och fukt ute har olika enheter. Därför är de **två diagram under varandra med samma tidsaxel**. Det blir aldrig dubbla y-axlar, eftersom det är det vanligaste sättet att lura läsaren.
- **Färger för diagram:** blå #2a78d6 och orange #eb6834. Paret är kontrollerat för färgblindhet och kontrast med dataviz-validatorn. Ute har dessutom streckad linje, så att färgen inte är det enda som skiljer dem åt.
- **Tolkningen står under diagrammet,** och man kan välja "Visa som tabell". I appen blir det ett tryck för att se veckans värden, som rutan "Slutet av juli".

## En graf per kort, med förhandsvisning och helskärm (10 november, Gustavs idé)
- **Kortet "Vädret och fukten":** rubriken med symbolen, **en liten förhandsvisning** av grafen utan axlar, med två linjer och prickar för händelser, och en rad som säger vad den visar. Hela kortet går att trycka på.
- **I helskärm:**
  - Period: 3 mån, 1 år, 2 år eller Allt.
  - Knappar för vilka linjer som syns, plus "+ Regn" för den som vill se mer.
  - Månader och år på axeln.
  - **Numrerade händelser** i grafen, till exempel avfuktare startad, konsulten mätte och byggde igen, och en lista under.
  - Tryck för att se en vecka.
  - "Vad grafen visar" i klartext.
  - "Visa som tabell".
  - Tipset att vrida telefonen.
- **Alltid samma enhet för inne och ute** (gram vatten per m³), så att båda linjerna delar samma axel.
- **Med avfuktare** visar grafen hur källaren går från "3 g över ute" före till "under 1 g över" efter ombyggnaden. Vattnet per vecka visas i kortet "Går det åt rätt håll?" och blandas inte in här.

## Grafen i premiumstil (10 november, förebild: Avanzas "Min utveckling")
- **Grafen fyller hela bredden och är hög,** cirka 400 px. Värdena på y-axeln står till höger och är små och dämpade. Rutnätet syns knappt.
- **Daglig data i stället för veckor,** så att linjerna får sin naturliga detalj.
- **Huvudlinjen (källaren) har en mjuk yta under sig** som tonar ut. Jämförelselinjen (ute) är tunnare och utan yta.
- **Överst:** en stor siffra som är *slutsatsen* ("+0,7 g över uteluften"), med "före"-värdet under. Teckenförklaringen står till höger.
- **Kontrollerna överst:**
  - g/m³ eller %
  - val av plats ("Torkrummet ▾")
  - "Jämför: Ute ▾", där man också kan välja ett annat rum
  - perioder: 3 mån, i år, 1 år, 2 år och Sedan start, där den valda har en ram
- **Händelserna** är numrerade prickar på linjen, och listan står under grafen.
- **Kortets förhandsvisning** har samma upplägg som Avanzas översikt: siffran till vänster, en liten graf med yta till höger och perioden som ett märke.

## Vad grafen ska svara på (10 november)
1. **Hjälpte åtgärden?** Jämför skillnaden mellan inne och ute före och efter en händelse.
2. **Kommer fukten inifrån eller utifrån?** Liten skillnad som följer ute betyder uteluften. Stor och jämn skillnad betyder en källa inne, till exempel marken.
3. **Är det säsongen eller ett problem?** På sommaren stiger fukten inne med ute. Jämför samma årstid år för år.
4. **Har något hänt?** Ett plötsligt hopp som ute inte har betyder läckage, tvätt eller vatten efter regn.
5. **Är det stabilt?** Låg, jämn skillnad i flera veckor betyder att det är dags att boka konsulten.
6. **Underlag** till konsulten, försäkringen eller en köpare.

**Nyckeltalet är skillnaden inne minus ute** (fukttillskott, g/m³). Förslag: ett läge som heter "Skillnad", med en enda linje där 0 betyder samma som ute. Det kan bli standardläget för vardagsanvändaren, medan två linjer blir läget för nördarna.

**Gränser:**
- Grafen visar inte fukt i material eller mögel, och den ställer ingen diagnos.
- Samband är inte orsak.
- **g/m³** visar *var fukten kommer ifrån*. **%** visar *risken* för mögel och kondens. Båda behövs.

## Regn: kommer fukten utifrån? (10 november)
Det finns två vägar in:
1. **Via luften:** regn gör uteluften fuktig, och den luften kommer in i källaren. Inne och ute stiger **samma dag**, och skillnaden mellan dem ändras inte. Det är normalt.
2. **Via marken:** regnvatten tränger genom marken in i betongen. Inne stiger **senare** och **mer än uteluften förklarar**, så skillnaden ökar. Det tyder på problem med dränering, stuprör eller hur marken lutar. Ingen källa anger hur lång fördröjningen är, så appen letar inom 0–7 dygn.

**Grafen:**
- Regnet visas som staplar i en egen remsa under linjerna, med samma tidsaxel. Det är aldrig en extra y-axel.
- Kortet "Regn och fukten" räknar ut hur mycket skillnaden ändras 1–3 dygn efter varje kraftigt regn (över 10 mm), före och efter en händelse.
- Exemplet: +1,1 g före stuprören förlängdes, och ingen tydlig ökning efter.
- **Kräver flera regn för att säga något.** Med en avfuktare igång syns regnet i avfuktarens vatten per dygn, inte i luften.

**Antagande A7 (ändrat):** om vatten tar sig in via marken växer skillnaden mot ute efter regn och ligger kvar. Fördröjningen är okänd. Testas när det finns minst 5 kraftiga regn i datan.

## Årstider och regn: regler efter research (10 november)
Underlaget finns i `research/fukt-regn-arstider.md`.
- **Två mått:** % visar risken nu (översikten, statusfärgen). Skillnaden mot ute i g/m³ visar varifrån fukten kommer (grafen).
- **Jämför aldrig vinter med sommar.** Jämför samma period förra året, eller skillnaden mot ute.
- **Sommarfukt är vanlig men riskabel.** Den visas som orange med en förklaring, inte som ett larm.
- **Ett enskilt regn tolkas inte.** Det krävs minst 5 kraftiga regn, och snösmältning räknas också.
- **Med avfuktare** syns vädret i avfuktarens kWh, inte i luften.
- **Mätfelet syns:** i läget "Skillnad" visas ett ljust band kring noll, "som ute", på ungefär ±0,5 g.
- **Status bygger på tid** över gränsen. Det blir beslut 0004.
- **Inga påhittade normalvärden** för årstiden. Uteluften är referensen.

## V9: grafen visar fukt från huset (10 november)
Ersätter V8-grafens två linjer som huvudvy.
- **Rubrik och svar först:** "Lite fukt från huset", +6 %, "Rummet har 59 %. Utan fukten från huset hade det haft 53 %", "Ner från +30 % när du började" och samma tid förra året.
- **Procent i stället för g/m³** (ändrat samma dag efter Gustavs feedback: "gm2, vad är det?"). Appen räknar i g/m³ men visar procentenheter vid rummets temperatur. g/m³ finns kvar under "Visa varför" och för nördarna.
- **En linje:** skillnaden inne minus ute, snitt per vecka. Årstidsvågen försvinner.
- **Grafen har tre nivåer med ord på axeln:** Som ute, Lite och Mycket, i stället för siffror.
- **Perioden när avfuktaren gick är skuggad,** och linjen ritas inte där, eftersom luften då visar avfuktaren och inte huset.
- **Händelser med namn** direkt i grafen ("Byggde om", "Stuprör").
- **Under grafen:** "Så har det gått" per period, "Regn och fukten" (4 av 6 före stuprören, 1 av 27 efter) och "Visa varför" med inne, ute och regn som ett eget diagram.
- **Nivåer (preliminära):** som ute under 5 %, lite 5–15 %, mycket över 15 % (ungefär 0,5 och 1,5 g/m³ vid 10 °C). Ska bli beslut 0004.

## V9: fliken Trend, "Så har det gått" (10 november)
Gustavs behov: "har jag haft appen i 3 år vill jag se hur det har gått i de olika rummen, med och utan avfuktare."
- **Nås via ikonen Trend i menyn** på översikten.
- **Överst en sammanfattning i ord:** "Huset har blivit torrare", med en rad per rum.
- **Vinter för vinter:** en tabell med rummen som rader och vintrarna (december–februari) som kolumner. Vintrar jämförs, eftersom vintern visar huset bäst.
- **Ett kort per rum med samma tidsaxel** (små diagram, ett per rum):
  - **Rum utan avfuktare:** fukt från huset i procent, med fälten "Som ute", "Lite" och "Mycket". Samma skala i alla sådana rum.
  - **Rum med avfuktare och smart uttag:** vattnet som avfuktaren tar bort, liter per dygn, som staplar per månad. Topparna på sommaren förklaras som vädret.
- **Händelser** som "Byggde om" och "Stuprör" står direkt i diagrammen.
- **Måtten blandas aldrig i samma diagram.** Varje rum har sitt mått, men alla har samma tidsaxel.

## V10: samma mall för alla rumssidor (10 november)
Löser punkterna 1, 2, 3, 7 och 8 i granskningen (research/insikter.md).
- **Ordningen på varje rumssida:** Nu → Går det åt rätt håll? → Varför? → Nästa steg → Visa mer. Det enda som skiljer rummen åt är måttet i "Går det åt rätt håll?":
  - **Med avfuktare och uttag:** vattnet som avfuktaren tar bort, tanken och kostnaden.
  - **Bara sensor:** fukt från huset i procent, med fälten "Som ute", "Lite" och "Mycket".
- **Jämförelser** görs alltid mot samma tid förra året och mot början.
- **Varför?** innehåller väderförklaringen i en mening, listan med händelser och knappen "Lägg till händelse".
- **Nästa steg:**
  - stegen sensor → avfuktare → uttag
  - tips bara när appen har sett en trend
  - en riktig källa i stället för en platshållare (Boverket om källare)
  - "Dags för konsulten?" när kurvan har planat ut
- **Garaget:** statusen är "Fuktigt för MC:n". Risken för rost räknas som dygn med över 80 % och över 0 °C, enligt definitionen av "time of wetness" i ISO 9223.
- **Demon har en tidslinje:** november 2029, tre år in. Översikten, rumssidorna och Trend-sidan använder samma påhittade data.
- **Kvar att göra:** helskärmsgrafer per rum med samma data (just nu länkar de till Trend-sidan), bytet när man lägger till en avfuktare och sidan för att lägga in en händelse.
- **Vädret tillbaka i "Varför?" (samma dag):** ett diagram över det senaste året med två linjer, båda i procent:
  - **Rummet:** den verkliga luftfuktigheten.
  - **"Med bara uteluftens fukt":** SMHI:s fukt omräknad till rummets temperatur.

  Avståndet mellan linjerna är fukten från huset, så det behövs ingen g/m³. I torkrummet ligger rummets linje still på 60 %, och staplarna under visar att avfuktaren får mer att göra när den streckade linjen ligger över 60 %.
- **Förhandsvisningar i Avanza-stil (samma dag, Gustavs förebild: Avanzas flik "Analys"):** "Går det åt rätt håll?" och "Varför?" är kort med rubrik, en pil ›, svaret i en mening och en liten graf utan y-axel. Hela kortet går att trycka på och öppnar en helskärmssida per rum (V10-Graf-…). Helskärmssidan innehåller:
  - väljare för rum och period
  - nuvärdet stort, med jämförelse mot starten och mot förra året
  - en stor graf med händelser
  - kortet "Vinter för vinter" med staplar
  - kortet "Varför?" med vädergrafen
  - händelserna

  Pilen gör det tydligt att man kan gå vidare.

## V11: enklare, tre nivåer (10 november)
Gustavs feedback: "för mycket funktioner, rörigt". Dessutom kom kortet "Varför?" igen när man tryckte vidare, och "Varför?" var en otydlig rubrik.
1. **Översikten** är bara snabbkollen: rummen och "Att titta på". Menyn med Trend och Händelser är borttagen. Kvar finns en knapp, +, för att lägga till.
2. **Rummet** har tre kort:
   - **Nu**
   - **Analys ›**, med svaret i en mening och en liten graf
   - **Nästa steg**, som bara visas när appen har något att säga
3. **Analys** (helskärm) är nördnivån. Där finns allt en gång:
   - stor graf med händelser och perioder
   - Vinter för vinter
   - Vädret (SMHI)
   - Händelser
   - Avfuktaren eller MC:n
   - Detaljer
- **Rubriken "Varför?" är borta.** Vädret heter "Vädret" och finns bara i analysen.
- **Trend-sidan (V9)** behövs inte längre. Varje rums analys har "Vinter för vinter".

## V12: två nivåer, och rummet är analysen (10 november)
Gustavs genomgång av V11:
- **Översikten:** bra. Garagekortet säger "Förhöjd", som de andra korten. "Fuktigt för MC:n" är borttaget från översikten. Raden "Dags för konsulten?" är också borttagen.
- **Rummet:** procenten har man redan sett på översikten. Därför står den bara som en rad överst: "● Bra · 60 % · 12 °C". Analysen fyller sidan:
  - svaret i en mening
  - det stora värdet och den stora grafen
  - Vinter för vinter
  - Vädret
  - Händelser
  - Avfuktaren eller MC:n
  - Detaljer
- **Tips bara när värdet är dåligt:** avfuktare i orörda rummet. Tipset om konsulten är borttaget, eftersom det var en gissning.
- **Statustexterna är regler, inte AI.** Till exempel ger "över 80 % och över 0 °C" texten "risk för rost". AI-texten ligger kvar i "senare" (beslut 0003).

## V13: en graf med två lägen, som filtren i Avanza (10 november)
Gustavs genomgång av V12-torkrummet: "1,3 l per dygn" var svårt att förstå. Meningen "Vintern visar huset bäst" var konstig. Vädret i en egen graf var svårt, och han vill inte ha många grafer.
- **En graf överst** med en väljare i två lägen. I Play-läget länkar knapparna mellan två ritytor.
  - **Huvudläget:**
    - *Tanken* i rum med avfuktare: hur många gånger i veckan tanken blir full. Nu 3, i början 9.
    - *Från huset* i rum utan avfuktare: fukt från huset i procent, med fälten "Som ute", "Lite" och "Mycket".
  - **Inne och ute:** rummets luftfuktighet (blå) och "med bara uteluftens fukt (SMHI)" (orange, streckad), båda i procent på samma axel. Avståndet mellan linjerna är fukten från huset.
- **Borttaget:** kortet "Vinter för vinter" (jämförelsen står i raden under värdet: "i början … förra november …") och kortet "Vädret" (vädret är nu ett läge i grafen).
- **Liter** finns bara kvar under Detaljer.
- **Kvar under grafen:** tips (bara om värdet är dåligt), Händelser, Avfuktaren eller MC:n, och Detaljer.
- **Rum med slang:** tanken går inte att räkna. Där behövs ett annat huvudmått, till exempel "jämfört med start". Det är inte bestämt än.

## V14: avfuktaren i timmar, vädret som filter (10 november)
Gustavs genomgång av V13: "Tanken" och "Inne och ute" var otydliga knappar. Många avfuktare töms dessutom automatiskt med slang. Grafen "Inne och ute" var svår att förstå för den som inte är insatt.
- **Rummet med avfuktare mäts i hur många timmar per dygn den går,** till exempel "5 tim per dygn, i början 16". Det smarta uttaget ser när avfuktaren går, så måttet fungerar med både tank och slang. Antagandet är cirka 250 W när den går (A10).
- **Grafen har en tydlig rubrik och en förklaring i stället för lägesknappar:**
  - "Hur mycket avfuktaren går. Ju mindre den behöver gå, desto mindre fukt kommer från huset."
  - "Fukt från huset. Vädret är borträknat, så det som syns är huset."
- **Vädret är ett filter, "Väder", i rummet med avfuktare.** Det skuggar perioder med fuktig uteluft, alltså när uteluften ensam hade gett rummet över 60 %. Det blir ingen andra skala, och man ser att topparna hamnar i de skuggade perioderna.
- **Rum utan avfuktare har inget väderfilter.** Vädret är redan borträknat, och statusraden säger "mest från uteluften".
- **Läget "Inne och ute" är borttaget.**

## V15: samma graf i alla rum, med val och filtret Väder (10 november)
Gustav: "på garaget vill man också ha fuktprocenten över tid … utgå från den här grafen, men med fler alternativ."
- **En graf per rum, samma design överallt.** Över grafen finns två val:
  - **Luftfuktighet:** rummets procent över tid, med en streckad gränslinje. Gränsen är 70 % i källaren och 80 % i garaget, där risken för rost börjar.
  - **Från huset** i rum utan avfuktare, eller **Avfuktaren** (timmar per dygn) i rum med avfuktare.
- **Startläget:** "Luftfuktighet" i rum utan avfuktare, eftersom det är den siffra man känner igen. I rum med avfuktare startar grafen på "Avfuktaren", eftersom procenten där är platt.
- **Filtret Väder:**
  - I läget Luftfuktighet lägger det till den streckade linjen "med bara uteluftens fukt (SMHI)". Båda linjerna är i procent, så de delar skala.
  - I läget Avfuktaren skuggar det perioder med fuktig uteluft.
  - Filtret döljs i läget Från huset, eftersom vädret redan är borträknat där.
- **Valen är riktiga:** radioknappar och CSS, så en rityta per rum räcker.
- **Insikt från datan:** i orörda rummet är procenten nästan densamma som första året (77 mot 78 %), eftersom hösten i år är fuktigare ute. Det är först "Från huset" som visar att huset har blivit bättre. Det är just därför båda valen behövs.
- **Förklaringen av "från huset" (samma dag):** under grafen i läget Från huset finns rutan "Vad betyder 'från huset'?". Den har:
  - en mening om de två hållen fukten kommer ifrån, uteluften och huset självt
  - en stapel med rummets egna siffror: uteluften ger 69 %, huset lägger till +8 %, tillsammans 77 %
  - en mening om varför husets del visar om huset blir torrare
  - nivåerna Som ute, Lite och Mycket

  Läget Avfuktaren har en liknande ruta, "Vad visar timmarna?". Linjen för Från huset är nu utjämnad över två veckor, och etiketten "Start" är borttagen.

## V16: rensad inför testet den 7 december (10 november)
Se beslut 0005. Borttaget: liter, tankstorlek, tank eller slang, Tapo, effekttexter vid händelser och "Uppdaterad 07:40". Översikten säger "Data till 9 nov · Ladda upp ny". Nytt:
- **Lägg till avfuktare:** procent, Shelly-uttag och elpris.
- **Lägg till händelse:** var, vad, när och en anteckning. Knappen + på översikten och knappen i Händelser leder hit.

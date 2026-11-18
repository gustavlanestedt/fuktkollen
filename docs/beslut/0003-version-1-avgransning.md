# 0003: Vad version 1 innehåller

**Datum:** 10 november 2026 · **Status:** beslutat efter tre prototyptest med Gustav (se research/insikter.md)

## Läge
- **Behoven:** det starkaste behovet är att se om fukten går åt rätt håll efter en åtgärd (B1). Varningarna (B3) löses redan av Govee och Shelly.
- **Testerna:** Gustav ville ha en enkel överblick per plats, och tryck för mer. Liter per dygn kändes godtyckligt, och riktningen och tanken var lättare att förstå.
- **Principen** är lågt golv och högt tak.

## Beslut
**Med i version 1:**
- **Översikten (version 7: stilen från version 4 utan hus):**
  - En statusrad överst med en prick: "Allt ser bra ut", eller "X platser behöver koll". Vädret är ett litet märke, "Ute 2°".
  - Kort i rutnät med namn, procent och status i ord och färg. Temperaturen visas inte här. Ett rum med avfuktare och uttag får ett högt kort med staplar från start till nu.
  - Listan "Att titta på" har en rad per plats som behöver koll.
  - 1–3 platser ligger under varandra, och 4 eller fler i två kolumner.
  - Temperaturen, vädret i detalj och det unika visas på platsens egen sida.
- **Rummets sida, med stegen sensor → avfuktare → smart uttag:**
  - **Bara sensor:** procent och jämförelse med uteluften, och tips när appen ser en trend.
  - **Med avfuktare och uttag:** "Går det åt rätt håll?" med en skala, tanken (eller jobbet, om den töms med slang), kostnaden och en kurva med händelser. Man väljer om kortet på översikten ska visa procent eller vatten.
  - Detaljer som g/m³ och kWh ligger bakom "Visa mer".
- **Lägg till avfuktare:** tank eller slang, tankens storlek, uttag, inställd luftfuktighet och elpris.
- **Händelser.**
- **Uppladdning för hand:** Govee-CSV och Shelly-data.
- **Ett publikt demoläge med påhittad data.** Dina egna data ligger bakom inloggning.

**Inte med i version 1:**
- egna larm
- automatisk import
- AI-texten
- onboarding, utöver import och "välj ort"
- fler användare
- visuell finputs

## Senare
- **Visuell finputs:** gör den när strukturen håller. Bygg med designtokens, alltså färger, typsnitt och avstånd i Tailwinds tema, så att det går snabbt att byta utseende.
- **Onboarding** för vardagsanvändaren.
- **Gränser för färgerna** med källor.

# 0001: Färdiga sensorer i stället för egen hårdvara

**Datum:** 9 november 2026 · **Status:** beslutat

## Läge
Appen behöver data över tid från källaren och garaget, med början innan uttorkningen startar. Det fanns två alternativ:
- **Egen hårdvara:** Raspberry Pi med Zigbee och Sonoff-sensorer. Den kostar 3 000–4 000 kr och tar flera kvällar att sätta upp.
- **Färdiga wifi-sensorer:** kostar cirka 1 000 kr och kan sättas upp direkt.

## Beslut
- **3 st Govee H5179**, placerade i rummet som torkar, i det orörda källarrummet och i garaget.
- **1 st Shelly Plug S Gen3** på avfuktaren, för att mäta energin.
- **FuktKollen blir ett lager som analyserar data** från färdiga sensorer, och ska inte vara bunden till ett märke.

## Konsekvenser
**Bra:**
- Datan samlas in från första dagen.
- Det är billigt.
- Govee och Shelly sköter larmen, så version 1 behöver inga egna larm.

**Mindre bra:**
- Govee-datan måste exporteras som CSV för hand, via e-post.
- Govee är beroende av sitt moln.
- Shellys lokala API går inte att nå från molnet. Automatisk import behöver en egen lösning senare.

Raspberry Pi med Zigbee finns kvar som alternativ senare, om du vill ha Home Assistant.

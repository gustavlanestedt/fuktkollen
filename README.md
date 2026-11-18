# FuktKollen

Följer fukten i huset över tid, räknar bort vädret och visar om åtgärderna hjälper.

## Varför
Jag har ett hus från 1934 med en fuktig källare. Sensorer visar procent här och nu, men inte om det blir bättre efter en åtgärd, eller om fukten kommer från huset eller från vädret. FuktKollen ska svara på just det.

## Status
Under utveckling. Version 1: översikt, rumssida med graf och uppladdning av data för hand.

## Teknik
Next.js, TypeScript, Tailwind CSS och öppna väderdata från SMHI.

## Köra lokalt
    npm install
    npm run dev

Öppna sedan http://localhost:3000.

## Dokumentation
Projektet började med problemet, inte med koden:
- [Brief](docs/brief.md): problem, användare och mål
- [Beslut](docs/beslut/): varför saker valdes
- [Antaganden](docs/antaganden.md): vad som ska testas
- [Research](docs/research/): intervju, insikter och fakta om fukt

## AI i arbetet
AI används för research, prototyper och rutinkod. Kärnlogiken skriver jag själv, och varje pull request säger vad AI gjorde.

## Licens
MIT
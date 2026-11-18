# 0002: Next.js, TypeScript och Vercel

**Datum:** 10 november 2026 · **Status:** beslutat

## Läge
Appen behöver kod på servern för att hämta från SMHI, ta emot uppladdade filer och prata med en databas. TypeScript, React och Next.js är kärnan i de flesta jobbannonser som är relevanta.

## Beslut
- **Next.js med App Router** och **TypeScript** i strikt läge, med Tailwind för stil.
- **Vercel** för publicering, med en förhandsversion för varje pull request.
- **Postgres** som databas, med migreringar. Leverantören väljs i specen, till exempel Neon eller Supabase.
- **Vitest** för enhetstester, **Playwright** för tester från början till slut och **axe** för tillgänglighet. Allt körs i **GitHub Actions**.

## Alternativ som valdes bort
- **Vite med separat backend:** fler delar att hålla ihop, utan någon vinst för en person.
- **.NET och Azure:** passar bättre för bokningsprojektet senare.

## Konsekvenser
**Bra:**
- En kodbas för både gränssnitt och server.
- Snabb publicering.
- Tränar precis det marknaden efterfrågar.

**Mindre bra:**
- Serverlösa funktioner har tidsgränser, så schemalagda jobb körs med Vercel Cron.
- Projektet blir delvis bundet till Vercel.

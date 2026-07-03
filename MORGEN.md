# 🚴 Morgen-prompt (fra telefonen, uden pc)

Åbn **claude.ai/code** i telefonens browser (eller Claude-appen), start en
cloud-session på repoet **Restrup/tdf-tourspillet**, og indsæt prompten
nedenfor. Sessionen kører i skyen — din pc kan være slukket.

---

> Det er morgen under Tour de France 2026. Dette repo er tourspillet-webappen
> (GitHub Pages). Gør følgende:
>
> 1. Find dagens etape ved at matche dagens dato mod STAGES-arrayets
>    date-felter i index.html (hviledage 13. og 20. juli: stop og sig det).
> 2. Søg på nettet efter dagens etape-vinderodds hos 2-3 bookmakere
>    (fx Bet365, Unibet, Betfair). Brug KUN odds du faktisk finder —
>    opfind aldrig tal. Ingen odds fundet → rør ikke filen, sig det.
> 3. Brug de PRÆCISE rytternavne fra RIDERS-arrayet i index.html.
> 4. Opdatér stage_odds.json — FLET dagens etape ind (bevar tidligere
>    etaper) i formatet:
>    {"ETAPENR": {"bookies": ["Bet365","Unibet"], "updated": "DD. mmm HH:MM",
>      "riders": [{"name": "Rytternavn", "odds": [x.xx, x.xx]}, ...]}}
>    med de 8-12 største favoritter. Validér JSON.
> 5. Commit og push stage_odds.json til main.
> 6. Slut med en kort dansk opsummering: etape, top 3-5 favoritter med
>    bedste odds og implicit vinderchance.

---

**Hvad sker der bagefter?** Appen (https://restrup.github.io/tdf-tourspillet/)
henter stage_odds.json automatisk — Bookmaker-odds-fanen opdateres for alle,
der åbner den. Ingen manuel indsætning.

**Pc'en tændt i stedet?** Så kører den planlagte opgave "tdf-morgen-odds"
selv kl. 07:30 (kræver at Claude-appen er åben) — samme resultat.

# flume

Seks skills for Claude, organisert som **én kaskade i to ledd**. Ikke seks separate verktøy, men en bevegelse: råmateriale tas imot, ordnes, og prosesseres fra utforsking til beslutning — uten å demme inne for tidlig.

Premisset er enkelt: en modell kan *moduleres gjennom faser* i stedet for å svare i ett. Et felt skal holdes i bevegelse mens det er uklart, og først stivne til en beslutning når det er modent. Skillene er stabile motorer; en egen master-instruks er dirigenten som bestemmer når hver motor trer inn, hvordan ledd henger sammen, og hvordan sløyfen lukkes.

## Struktur

**Sluse-ledd** (inntak):
1. `companai-01-catch` — fanger og bevarer råtekst ordrett, uten mappevalg.
2. `companai-02-tidy` — grovsorterer fangede blokker, foreslår klynger og triage.

→ *et felt trer fram* — en klynge som kjennes verdt å se nærmere på krysser inn i strøm-leddet.

**Strøm-ledd** (prosessering):
3. `currents-01-scout-core` — speider i feltet uten å konkludere.
4. `currents-02-regime-mapper` — mapper 2–5 regimer feltet veksler mellom.
5. `currents-03-hypothesis-hook` — henger små, testbare hypoteser på regimene.
6. `currents-04-decision-log-writer` — gjør én hypotese om til en kort, revidérbar beslutning.

Beslutningen lukker ikke bevegelsen — den setter en sluse med åpen revisjon. Når revisjonen slår til, behandles observasjonen som en ny fangst. Sløyfen lukkes, men slutter ikke.

## Faste prinsipper

- **Råtekst er hellig.** Fanget råtekst bevares ordrett, aldri omskrevet eller slettet uten bekreftelse. Friheten til å omarbeide fritt hviler på at originalen aldri går tapt.
- **Foreslå, ikke utfør.** Triage, arkivering og sletting skjer som forslag brukeren bekrefter.
- **Ikke demm inne for tidlig.** Hold feltet i bevegelse i de tidlige leddene; spar konklusjoner til beslutningsleddet.
- **Konstruktiv svak støy.** Behold faste skjemaer, men la overflatespråk variere litt mellom kjøringer, så outputen ikke kollapser til mal.

## Bruk

Hver skill er en `SKILL.md` med standard frontmatter (`name` + `description`) — gyldig som de står, uten avhengigheter eller scripts. Legg `skills/`-mappene der Claude leser skills fra, eller pakk dem som `.skill`-filer for enklere installasjon.

`master-instruks.md` er orkestreringslaget — den nøytrale ryggen som binder de seks sammen. Modulasjonslaget (tone og friksjon) og eventuell prosjektkontekst legges inn i de merkede slissene nederst i instruksen, ikke i skillene. Slik holdes motorene stabile mens dirigenten kan byttes ut per prosjekt.

## Status

Eksperimentell (v0.1–0.2). Skillene er på norsk bokmål. Delt for å utforske ideen om faseinndelt modulasjon — bevegelse framfor enkeltsvar — og for å se hva andre gjør med beslektede mønstre. Tilbakemeldinger og forgreininger er velkomne.

## Forfatter & lisens

Pål-Stian Misje.

Lisensiert under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Du står fritt til å bruke, dele og bygge videre — også kommersielt — så lenge du krediterer opphavet. Se `LICENSE`.

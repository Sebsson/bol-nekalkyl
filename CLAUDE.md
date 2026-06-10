# CLAUDE.md

Vägledning för Claude när det jobbar i detta repo.

## Git-arbetsflöde

- **Hämta alltid senaste git-status först.** I början av varje arbetspass, kör
  `git fetch` och `git status` (och `git pull --ff-only` om `origin/main` ligger
  före) innan några ändringar görs, så att arbetet utgår från senaste versionen.
- **Committa och pusha automatiskt.** När en ändring är klar och accepterad:
  committa med ett tydligt meddelande och pusha till `origin/main` utan att fråga
  – om inte användaren uttryckligen ber att en viss ändring *inte* ska pushas.
- Branch: `main`. Remote: `origin`
  (https://github.com/Sebsson/bol-nekalkyl.git).

## Om projektet

- En enda fristående HTML-fil: `bolanekalkyl.html`. All CSS och JavaScript är
  inbyggd, Tailwind via CDN, Inter som typsnitt. Inget byggsteg.
- Skandinavisk, modern och lugn estetik med mycket whitespace.
- Svensk talformatering rakt igenom: mellanslag (U+00A0) som tusentalsavgränsare,
  komma som decimaltecken, `kr`/`%` med fast mellanslag före enheten.

## Konventioner

- Behåll allt i en fil – inga externa beroenden utöver CDN.
- Bevara den svenska talformateringen och den befintliga visuella hierarkin.
- PDF-/utskriftsläget ska rymmas på en sida och vara utan ram
  (se `@media print` i filen).

## Lokal förhandsvisning

- Statisk server via `.claude/launch.json` (`python -m http.server 8123`).
- Öppna `http://localhost:8123/bolanekalkyl.html`.

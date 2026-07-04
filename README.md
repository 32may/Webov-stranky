# Webové stránky – startovací repozitář

Tento repozitář slouží jako přehledná výchozí šablona pro nové webové projekty.

## Jak ho používat

1. Každý skutečný web má vlastní repozitář.
2. Zadání práce patří do GitHub Issues.
3. Každá změna má vlastní větev a Pull Request.
4. `main` představuje oficiální funkční verzi.
5. Hesla, API klíče a zákaznická data se do GitHubu nikdy neukládají.

## Struktura

- `src/` – zdrojový kód webu
- `content/` – články, kurzy a další obsah
- `tests/` – automatické testy
- `docs/` – architektura, provoz a rozhodnutí
- `.github/` – šablony úkolů, Pull Requestů a automatizace
- `AGENTS.md` – pravidla pro Codex, Claude a další agenty
- `.env.example` – seznam potřebných proměnných bez skutečných tajných hodnot

## Doporučený tok práce

`Issue → větev → změny → testy → Pull Request → kontrola → merge`

## Stav repozitáře

Repozitář je připravený jako základ pro webové projekty. Název lze později změnit na `web-starter` a v nastavení GitHubu jej označit jako Template repository.
# GitHub ekosystém

Tento dokument popisuje, jak má být GitHub účet uspořádaný, jakou roli mají jednotlivé repozitáře a jak v nich mají pracovat lidé i AI agenti.

## Základní logika

- Jeden osobní GitHub účet představuje konkrétního člověka.
- Organizace sdružuje repozitáře jedné firmy nebo většího projektu.
- Jeden samostatný produkt, web nebo aplikace má vlastní repozitář.
- Jeden repozitář není určený pro jednoho agenta; na stejném projektu mohou pracovat Codex, Claude Code i člověk.
- `main` je jediná oficiální funkční verze projektu.
- Každý větší úkol má vlastní Issue, větev a Pull Request.

## Aktuální členění účtu

### `Webov-stranky`

Budoucí startovací šablona pro nové webové projekty. Doporučený budoucí název je `web-starter`.

Obsahuje společnou strukturu, dokumentaci, pravidla agentů a pracovní šablony. Nemá sloužit jako jeden velký repozitář pro všechny budoucí weby. Každý skutečný web vytvořený podle této šablony má dostat vlastní repozitář.

### `Pokusy`

Bezpečné pískoviště pro učení GitHubu, malé prototypy a krátké experimenty.

Jakmile se z pokusu stane samostatný dlouhodobý produkt, přesune se do vlastního repozitáře.

### `Had-game`

Samostatný hotový projekt. Patří do vlastního repozitáře, protože má vlastní účel, kód a životní cyklus.

## Doporučené budoucí členění

```text
32may – osobní účet
│
├── may-labs – organizace pro experimenty a společné nástroje
│   ├── web-starter
│   ├── agent-templates
│   ├── automation-library
│   └── experiments
│
├── naucime-ai – firemní organizace
│   ├── public-web
│   ├── academy-platform
│   └── internal-automations
│
└── samostatné osobní projekty
    └── Had-game
```

Organizace se mají zakládat podle skutečných firem nebo dlouhodobých oblastí. Není potřeba vytvářet organizaci pro každý malý pokus.

## Co patří do repozitáře

- zdrojový kód,
- technická dokumentace,
- testy,
- konfigurace bez tajných hodnot,
- šablony úkolů a Pull Requestů,
- instrukce pro agenty,
- anonymizovaná testovací data,
- textový obsah, pokud se spravuje společně s kódem.

## Co do repozitáře nepatří

- hesla a přístupové tokeny,
- skutečné hodnoty API klíčů,
- produkční databáze,
- zákaznická a účetní data,
- faktury,
- soukromé exporty,
- osobní údaje bez jasného důvodu a ochrany.

## Doporučená struktura repozitáře

```text
projekt/
├── README.md
├── AGENTS.md
├── src/
├── content/
├── tests/
├── docs/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── pull_request_template.md
│   └── workflows/
└── .gitignore
```

### Význam hlavních souborů

- `README.md` – rychlá orientace pro člověka.
- `AGENTS.md` – pravidla pro Codex, Claude Code a další agenty.
- `docs/` – hlubší dokumentace a důležitá rozhodnutí.
- `.github/` – pracovní šablony a automatické kontroly.
- `src/` – programový kód.
- `tests/` – automatické kontroly.

## Jak pracují agenti

Codex, Claude Code ani jiný agent nemají vlastní paralelní projekt. Pracují nad stejným repozitářem jako člověk.

Doporučený postup:

```text
Issue
→ pracovní větev
→ změny a commity
→ testy
→ Pull Request
→ lidská kontrola
→ merge do main
```

Každý agent má mít pouze oprávnění, která skutečně potřebuje. Automatický agent nemá mít možnost mazat repozitáře, měnit fakturaci nebo provádět nevratné produkční akce bez lidského potvrzení.

## Pracovní pojmy

- **Repozitář** – jedna samostatná věc, kterou stavíme.
- **Issue** – zadání, chyba nebo nápad.
- **Větev** – bezpečný prostor pro jednu změnu.
- **Commit** – pojmenovaný uložený krok.
- **Pull Request** – návrh změny ke kontrole.
- **Merge** – schválené připojení změny do hlavní verze.
- **main** – oficiální aktuální verze.
- **GitHub Project** – společná nástěnka úkolů.

## Praktická pravidla

1. Jeden produkt má vlastní repozitář.
2. Jeden úkol má vlastní větev.
3. Jeden Pull Request má jeden hlavní účel.
4. `main` se nemění přímo, pokud to není nouzová výjimka.
5. Agent před prací čte `README.md` a `AGENTS.md`.
6. Automatické kontroly mají proběhnout před připojením změny.
7. Produkční nasazení a nevratné akce vyžadují lidskou kontrolu.
8. Tajné hodnoty se ukládají mimo GitHub do správce secrets.

## Cílový stav

- `Webov-stranky` přejmenovat na `web-starter`.
- Označit jej jako Template repository.
- Vytvořit organizaci `may-labs`.
- Vytvořit samostatný repozitář `agent-templates` pro sdílená pravidla agentů.
- U hlavních repozitářů chránit větev `main` a vyžadovat Pull Request.
- `Had-game` ponechat jako samostatný projekt a jeho vstupní soubor později přejmenovat na `index.html`.

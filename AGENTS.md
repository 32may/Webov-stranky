# Pravidla pro AI agenty

Tato pravidla platí pro Codex, Claude Code i další automatické pracovníky.

## Povinný postup

1. Před změnou si přečti `README.md` a relevantní dokumentaci v `docs/`.
2. Jeden úkol řeš jako jednu samostatnou změnu.
3. Neměň soubory mimo rozsah zadání bez vysvětlení.
4. Zachovej existující funkčnost, pokud zadání výslovně neříká opak.
5. Po změně spusť dostupné kontroly a testy.
6. Popiš, co se změnilo, proč a jak bylo řešení ověřeno.

## Bezpečnost

- Nikdy neukládej hesla, tokeny, osobní údaje ani produkční data.
- Skutečné hodnoty proměnných prostředí patří do správce secrets, nikoli do repozitáře.
- Neprováděj platby, mazání produkčních dat ani jiné nevratné akce bez lidského schválení.
- Nepřidávej novou službu nebo závislost bez zdůvodnění.

## Kvalita

- Preferuj malé, čitelné změny.
- Nevytvářej duplicitní komponenty a utility.
- Aktualizuj dokumentaci, pokud měníš strukturu, provoz nebo veřejné chování projektu.
- Novou funkčnost doplň testem, pokud je to rozumně možné.

## Výstup agenta

Na konci práce uveď:

- změněné soubory,
- provedené testy,
- známá omezení,
- případné kroky vyžadující lidské rozhodnutí.
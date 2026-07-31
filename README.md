# Budapest Grand Prix — generátor kartiček

Jeden soubor, žádné závislosti, žádný build. `index.html` otevřeš i lokálně dvojklikem.

## Nasazení na GitHub Pages

1. Nový repozitář, nahraj `index.html` (a klidně i `budapest-jetlag.md` jako pravidla).
2. **Settings → Pages → Source: Deploy from a branch → `main` / `root`** → Save.
3. Za minutu běží na `https://<uživatel>.github.io/<repo>/`.

Odkaz si pak všichni čtyři uložte na plochu telefonu (Safari: Sdílet → Přidat na plochu). Chová se to pak jako appka.

## Jak se to používá

- **Čtyři balíčky** = čtyři linky metra: Kérdés (otázky), Átok (prokletí), Feladat (úkoly), Szobor (sošky).
- **Húz** táhne kartu. Tažená karta se do balíčku nevrací, dokud nedáš **Zamíchat**.
- **Cokoliv** táhne z náhodného balíčku — dobré, když chcete jen chaos.
- U otázek jdou zapnout **filtry kategorií** (jen fotky, jen radar, …).
- U sošek je checklist: klepnutím na **A** / **B** přiřadíš sošku týmu a body naskočí do skóre dole.
- **Ctrl/Cmd + P** vytiskne všechny karty na arch k rozstříhání, pokud je chcete fyzicky.

## Stav hry

Skóre, tažené karty i sošky se ukládají **do adresy stránky** (za `#`). Refresh je nesmaže. Když chcete mít stejný stav na druhém telefonu, prostě si pošlete aktuální odkaz.

Praktický režim: **každý tým jedno zařízení, oba mají vlastní stav.** Hledající tým si tahá otázky, hledaný tým prokletí.

## Editace karet

Všechna data jsou nahoře ve `<script>` v objektu `DECKS`. Přidat kartu = přidat řádek:

```js
{t:'Text karty, <em>zvýraznění</em> takhle.', k:'Kategorie', p:5}
```

- `t` — text (může obsahovat HTML)
- `k` — kategorie / u sošek adresa
- `p` — body (nepovinné, může být i záporné)
- `n` — poznámka pod textem (u otázek např. „ano/ne“)

Nic dalšího měnit netřeba, ID karet i filtry se dopočítají samy.

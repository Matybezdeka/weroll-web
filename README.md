# weroll studio – web

Jednostránkový web: logo → klienti jedoucí zprava → „Momentálně nebereme nové zakázky." → kontakt.

## Co je ve složce

| Soubor | K čemu je |
|---|---|
| `index.html` | celý web (HTML, CSS i JavaScript v jednom souboru) |
| `logo.webp` | logo weroll studio (bílé, průhledné pozadí – web si ho sám obarvuje) |
| `fonts/kumbh-sans-latin.woff2` | brandový font Kumbh Sans (základní znaky) |
| `fonts/kumbh-sans-latin-ext.woff2` | Kumbh Sans – česká diakritika (ě, š, č, ř, ž, ů…) |
| `README.md` | tento návod |

Všechny soubory musí zůstat ve stejné struktuře (složka `fonts` vedle `index.html`).

## Jak web dát na GitHub a zveřejnit (GitHub Pages) – bez instalace čehokoliv

1. Přihlas se na **github.com** (nebo si založ účet).
2. Vpravo nahoře klikni na **+** → **New repository**.
   - *Repository name:* např. `weroll-web`
   - nastav **Public** (GitHub Pages zdarma funguje jen pro veřejné repozitáře)
   - klikni **Create repository**.
3. Na stránce nového repozitáře klikni na odkaz **uploading an existing file**.
4. Rozbal ZIP a **přetáhni do okna celý obsah složky** (`index.html`, `logo.webp`, `README.md` a složku `fonts`).
   Pozor: přetahuj obsah složky, ne složku samotnou – `index.html` musí být v kořeni repozitáře.
5. Dole klikni **Commit changes**.
6. Jdi do **Settings** → v levém menu **Pages**.
   - *Source:* **Deploy from a branch**
   - *Branch:* **main**, složka **/ (root)** → **Save**.
7. Za 1–2 minuty bude web na adrese `https://TVUJ-UCET.github.io/weroll-web/` (odkaz se objeví nahoře na stránce Pages).

## Vlastní doména (např. weroll.studio)

1. V **Settings → Pages → Custom domain** napiš doménu (např. `weroll.studio`) a dej **Save**.
2. U registrátora domény nastav DNS:
   - pro `weroll.studio` čtyři **A** záznamy: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - pro `www.weroll.studio` **CNAME** záznam na `TVUJ-UCET.github.io`
3. Po propsání DNS (minuty až hodiny) zaškrtni v Pages **Enforce HTTPS**.

## Úpravy

- **Klienti:** v `index.html` hledej `<span class="client">` – každý řádek = jeden klient. Přidat/odebrat stačí zkopírováním/smazáním řádku.
- **Barvy:** nahoře v `index.html` v bloku `:root` (`--red` je hlavní barva #EB564F).
- **Kontakt:** sekce `<!-- 3) kontakt -->`.
- **Délka jízdy klientů:** `.ride { height: 640vh; }` – vyšší číslo = pomalejší jízda.

Změny se dají dělat přímo na GitHubu: klikni na soubor → ikona tužky → uprav → **Commit changes**. Web se sám aktualizuje do minuty.

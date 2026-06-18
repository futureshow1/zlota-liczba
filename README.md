# SECTIO AUREA — interaktywny atlas Złotej Liczby

Edukacyjny portal 3D o złotej liczbie (φ) i matematyce proporcji — od pitagorejskiej
geometrii po fizykę quasikryształów. Rygor oddzielony od romantycznej numerologii.
Przedmiotem jest **złota liczba**, a Matila Ghyka — jednym z filarów, nie jedynym autorem.

## Strony (samodzielne, bez build-stepu)

| Plik | Rola |
|---|---|
| `index.html` | **Strona główna** — dwunastościan-nawigator (12 ścian = 12 komnat) |
| `atlas.html` | Atlas (lista 12 komnat) + grywalna Komnata Ogród (filotaksja) |
| `liczba.html` | Komnata I — Tetraktys jako instrument (audio) |
| `proporcja.html` | Komnata II — odkryj φ, wirujące kwadraty, Fibonacci |
| `pentada.html` | Komnata III — pentagram, nieskończone zejście, shader quasikryształu |
| `bryly.html` | Komnata IV — bryły platońskie 3D + quiz |
| `loza.html` | Komnata X — konstelacja przekazu wiedzy 3D + gra |
| `probierz.html` | Komnata XII — kamień probierczy: gra obalania mitów |
| `filary.html` | Filary — kolumnada 3D ośmiu myślicieli |
| `progress.js` | Wspólny system złota/rang/odznak (Skarbiec, localStorage) |

Zależności zewnętrzne: three.js 0.165 i Google Fonts z CDN (wymagają internetu).

## Uruchomienie lokalne

```bash
python3 -m http.server 8137
# otwórz http://localhost:8137/
```
(Wymagany serwer HTTP — pliki używają modułów ES; otwarcie przez `file://` nie zadziała.)

## Deploy na GitHub Pages

To czysty statyczny site — wystarczy wypchnąć folder i włączyć Pages:

```bash
cd "ghyka-zlota-liczba"
git init && git add -A && git commit -m "SECTIO AUREA"
git branch -M main
git remote add origin git@github.com:<TWÓJ-LOGIN>/sectio-aurea.git   # repo trzeba najpierw utworzyć na GitHub
git push -u origin main
```
Następnie: **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `(root)`**.
Po chwili portal będzie pod `https://<TWÓJ-LOGIN>.github.io/sectio-aurea/`.
Plik `.nojekyll` jest już dodany (wyłącza przetwarzanie Jekyll).

> Publikacja jest akcją po Twojej stronie (konto GitHub + utworzenie repo) — stąd kroki, a nie automat.

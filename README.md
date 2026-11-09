# The Witchy Sewing Club

Strona zapisów na andrzejkowy wieczór w pracowni Shvoov Eco Deco (sobota 28.11.2026, 18:00–21:00, Warszawa).

Statyczna strona: jeden plik `index.html` plus obrazki. Nie wymaga budowania.

## Pliki

- `index.html`: cała strona (PL/EN, ekran startowy, animacje, płatności)
- `cover.jpg`: grafika wydarzenia
- `og.jpg`: obrazek podglądu linku (Facebook, Messenger, WhatsApp)
- `favicon.svg`: ikonka w karcie przeglądarki

## Jak zmienić liczbę wolnych miejsc

W `index.html` znajdź na dole blok `CONFIG` i zmień `spotsLeft`:

```js
const CONFIG = {
  formUrl: "...",
  spotsTotal: 10,
  spotsLeft: 10,   // ← tu wpisz, ile miejsc zostało
  eventStart: "2026-11-28T18:00:00+01:00"
};
```

Przy `spotsLeft: 0` strona pokaże „Komplet”, a świeczki zgasną.

## Vercel

1. vercel.com → Add New → Project → wybierz repo `JUSTYNA`.
2. Framework Preset: **Other**. Build Command i Output Directory zostaw puste.
3. Deploy.

Po wdrożeniu możesz w `index.html` zmienić adres w `og:image` na `https://TWOJA-DOMENA/og.jpg`.

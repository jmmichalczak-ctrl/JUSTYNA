# The Witchy Sewing Club

Strona zapisów na andrzejkowy wieczór w pracowni Shvoov Eco Deco (sobota 28.11.2026, 18:00–21:00, Warszawa).

Statyczna strona: jeden plik `index.html` plus obrazki. Nie wymaga budowania.

## Pliki

- `index.html`: cała strona (PL/EN, ekran startowy, animacje, płatności)
- `cover.jpg` (1800 px) i `cover-1200.jpg`: grafika wydarzenia; przeglądarka sama wybiera ostrzejszą wersję na ekranach retina
- `og.jpg` (1200×630): obrazek podglądu linku (Facebook, Messenger, WhatsApp, Instagram)
- `favicon.svg`, `apple-touch-icon.png`: ikonki w karcie przeglądarki i na ekranie iPhone'a
- `vercel.json`: ustawienia cache dla Vercel

## Podgląd linku na Facebooku

Facebook zapamiętuje podgląd linku. Jeśli zobaczysz stary obrazek albo brak obrazka, wklej link na
https://developers.facebook.com/tools/debug/ i kliknij „Scrape Again”.

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

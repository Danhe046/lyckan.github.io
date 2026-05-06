# Lyckan - Förskola & Fritids i Näshult

Webbplats för Föräldrakooperativet Lyckan, byggd med Jekyll och hostad på GitHub Pages.

## Lokal utveckling

1. Installera Ruby (https://www.ruby-lang.org/)
2. Kör:
```bash
bundle install
bundle exec jekyll serve
```
3. Öppna http://localhost:4000

## Redigera innehåll

Alla sidor skrivs i Markdown (`.md`-filer). Redigera texten direkt och pusha till GitHub – sidan byggs automatiskt.

## Anpassad domän

När du är redo att flytta domänen `föräldrakooplyckan.se`:
1. Lägg till en fil `CNAME` med innehållet: `föräldrakooplyckan.se`
2. Konfigurera DNS hos din domänregistrar (peka mot GitHub Pages IP-adresser)
3. Aktivera HTTPS i repository Settings → Pages

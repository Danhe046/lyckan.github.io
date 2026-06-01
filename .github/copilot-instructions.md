# GitHub Copilot Instructions – Lyckan Förskola & Fritids

## Projektöversikt

Statisk webbplats för **Föräldrakooperativet Lyckan** – en förskola och ett fritids i Näshult, Vetlanda kommun. Byggd med **Jekyll** och hostad på **GitHub Pages** via den anpassade domänen `föräldrakooplyckan.se`.

## Teknikstack

- **Jekyll** (statisk webbplatsgenerator, Markdown + Liquid-mallar)
- **HTML/CSS/JS** – inga externa ramverk, egen CSS med CSS-variabler
- **Google Fonts** – Baloo 2 (rubriker) och Nunito (brödtext)
- **GitHub Pages** för hosting

## Språk och ton

- Allt innehåll skrivs på **svenska**
- Tonen är **varm, inbjudande och lekfull** – riktar sig till föräldrar och barn
- Använd ett enkelt och tydligt språk, undvik byråkratiska formuleringar

## Projektstruktur

```
_config.yml          – Jekyll-konfiguration, navigationsstruktur
_layouts/            – Sidmallar: default.html, home.html, page.html
_includes/           – Återanvändbara delar: header.html, footer.html
assets/css/          – style.css (enda stilmall)
assets/images/       – Bilder till webbplatsen
assets/js/           – main.js
index.html           – Startsidan (layout: home)
om-oss.md            – Om oss-sidan
kontakt.md           – Kontaktsida
faciliteter.md       – Övergripande facilitetsida
faciliteter/         – Undersidor: inomhus.md, garden.md, narmiljon.md
personuppgifter.md   – GDPR-sida
```

## Designsystem (CSS-variabler)

```css
--color-primary:       #2F7DAE   /* blå, huvudfärg */
--color-primary-light: #5BA3D9
--color-secondary:     #F7B731   /* gul */
--color-accent-green:  #4CAF50
--color-accent-pink:   #E91E63
--color-accent-orange: #FF9800
--color-accent-purple: #9C27B0
--color-bg:            #FFFDF7
--color-bg-alt:        #FFF8E7
--font-heading:        'Baloo 2', cursive
--font-body:           'Nunito', sans-serif
--radius:              12px
--radius-lg:           20px
```

Använd alltid CSS-variabler i stället för hårdkodade färger eller typsnitt.

## Konventioner

- **Markdown-sidor** ska alltid ha front matter med `layout`, `title` och `permalink`
- **Bilder** placeras i `assets/images/` och refereras med `{{ site.baseurl }}/assets/images/filnamn.jpg`
- **Interna länkar** i Markdown skrivs med `{{ site.baseurl }}/sökväg/` eller Liquid-filtret `relative_url`
- Sektioner i HTML-sidor använder klasserna `.section` och `.section-alt` för alternerande bakgrunder
- CTA-knappar skrivs som `[Text →](url){: .btn}` i Markdown

## Barngrupperna

- **Igelkottarna** – yngsta barnen (nedervåningen)
- **Ugglorna** – äldre förskolebarnen (övervåningen)
- **Fritidsbarnen** – har egna områden och aktiviteter

## Vad du ska undvika

- Lägg inte till externa CSS-ramverk (Bootstrap, Tailwind o.s.v.)
- Lägg inte till JavaScript-beroenden utan att fråga
- Ändra inte `CNAME`-filen (hanterar den anpassade domänen)
- Skriv inte innehåll på andra språk än svenska

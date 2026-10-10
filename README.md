# gutshaus-kleinmenow.de

Website für das Gutshaus Kleinmenow (Villa Meteor) bei Fürstenberg/Havel. Sie stellt das Haus vor und dient dem Verkauf der drei Wohnungen im Obergeschoss.

Live: **https://gutshaus-kleinmenow.de**

## Wie das hier läuft

- **Timm** (`timimmo`) liefert Inhalte und Wünsche als [Issues](../../issues): Texte, Fotos, PDFs, Links, Korrekturen. Jedes Issue sollte kurz sagen, was damit passieren soll.
- **Björn** (`dasboe`) setzt die Issues um. Jeder Push auf `main` geht nach etwa einer Minute live.

## Aufbau

Reines HTML und CSS, kein Build-Schritt, kein JavaScript. GitHub Pages liefert den Inhalt von `main` direkt aus.

```
index.html          Startseite (Projekt, Wohnungen, Haus, Lage, Chronik, Kontakt)
impressum.html
datenschutz.html
404.html
assets/css/         Stylesheet
assets/fonts/       Mazius Display und EB Garamond, selbst gehostet (SIL OFL)
assets/img/         Fotos als WebP in drei Größen, Grundriss, Vorschaubild
dokumente/          Grundriss Obergeschoss als PDF
CNAME               Eigene Domain für GitHub Pages
```

Alles in diesem Repository ist öffentlich und unter der Domain abrufbar, auch PDFs.

## Bilder nachliefern

Neue Fotos am besten in voller Auflösung als Issue-Anhang. Sie werden dann verkleinert und als WebP in `assets/img/` abgelegt (480, 960 und bis 1600 Pixel Breite).

## Schriften

- [Mazius Display](https://github.com/collletttivo/Mazius-Display), Collletttivo, SIL OFL 1.1
- [EB Garamond](https://github.com/georgd/EB-Garamond), Georg Duffner und Octavio Pardo, SIL OFL 1.1

# gutshaus-kleinmenow.de

Website für das Gutshaus Kleinmenow (Villa Meteor) bei Fürstenberg/Havel. Sie stellt das Haus vor und dient dem Verkauf der drei Wohnungen im Obergeschoss.

Live: **https://gutshaus-kleinmenow.de**

**Selbst pflegen:** Preise, Status der Wohnungen, Telefonnummer, E-Mail, Kleinanzeigen-Link und das Stand-Datum stehen in der Datei `_data/inhalt.yml`. Wie man sie im Browser ändert, steht in [WARTUNG.md](WARTUNG.md).

## Wie das hier läuft

- **Timm** (`timimmo`) ändert die Werte in `_data/inhalt.yml` selbst. Alles andere (Texte, Fotos, PDFs, Links, Korrekturen) liefert er als [Issue](../../issues). Jedes Issue sollte kurz sagen, was damit passieren soll.
- **Björn** (`dasboe`) setzt die Issues um, schaut aber nur noch ab und zu rein. Jeder Push auf `main` geht nach etwa einer Minute live.

## Aufbau

HTML und CSS, kein JavaScript. GitHub Pages baut die Seite mit dem dort eingebauten Jekyll: Die sechs HTML-Seiten enthalten Platzhalter, die beim Bau mit den Werten aus `_data/inhalt.yml` gefüllt werden. Kein eigener Build-Schritt, keine Abhängigkeiten.

```
_data/inhalt.yml    Die Werte, die sich ändern (Preise, Status, Kontakt, Links, Stand)
_config.yml         Einstellungen für den Bau, muss nicht angefasst werden
WARTUNG.md          Anleitung für Timm
index.html          Startseite (Projekt, Wohnungen, Haus, Lage, Chronik, Kurz gefragt, Kontakt)
impressum.html
datenschutz.html
404.html
en/                 Englische Fassung der drei Seiten
assets/css/         Stylesheet
assets/fonts/       Mazius Display und EB Garamond, selbst gehostet (SIL OFL)
assets/img/         Fotos als WebP in drei Größen (480, 960, 1600 px), Grundriss, Vorschaubild
dokumente/          Grundriss Obergeschoss als PDF
CNAME               Eigene Domain für GitHub Pages
```

Alles in diesem Repository ist öffentlich und unter der Domain abrufbar, auch PDFs.

## Bilder nachliefern

Neue Fotos am besten in voller Auflösung als Issue-Anhang. Sie werden dann verkleinert und als WebP in `assets/img/` abgelegt (480, 960 und bis 1600 Pixel Breite).

## Schriften

- [Mazius Display](https://github.com/collletttivo/Mazius-Display), Collletttivo, SIL OFL 1.1
- [EB Garamond](https://github.com/georgd/EB-Garamond), Georg Duffner und Octavio Pardo, SIL OFL 1.1

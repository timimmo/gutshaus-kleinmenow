# Die Seite selbst pflegen

Diese Anleitung ist für Timm. Sie erklärt, wie du Preise, Status, Telefonnummer und Links auf gutshaus-kleinmenow.de selbst änderst, ohne jemanden zu fragen. Alles, was sich regelmäßig ändert, steht in einer einzigen Datei: `_data/inhalt.yml`. Die Seite (deutsch und englisch) holt sich die Werte von dort.

## 1. Etwas ändern, drei Schritte

1. Öffne diesen Link: **https://github.com/timimmo/gutshaus-kleinmenow/edit/main/_data/inhalt.yml** (du musst bei GitHub angemeldet sein).
2. Ändere nur den Text zwischen den Anführungszeichen. Zeilen nicht löschen, Anführungszeichen stehen lassen. Beispiel: aus `preis_we6: ""` wird `preis_we6: "195.000 €"`.
3. Klick oben rechts auf den grünen Knopf **Commit changes**, dann im Fenster noch einmal auf den grünen Knopf **Commit changes**. Fertig. Nach etwa einer Minute ist die Änderung auf https://gutshaus-kleinmenow.de zu sehen, deutsch und englisch. Lade die Seite neu, falls du noch den alten Stand siehst.

Das geht auch am Handy im Browser, ist dort aber fummelig.

## 2. Welche Zeile wofür

| Zeile | Was sie auf der Seite macht | Erlaubte Werte |
|---|---|---|
| `stand` | „Stand 10/2026“ unten auf jeder Seite, das Jahr im © | Monat/Jahr, zum Beispiel `"11/2026"` |
| `telefon` | Telefonnummer im Kontakt und im Impressum | Die Nummer, so wie sie stehen soll. `""` (leer) blendet sie aus |
| `mail` | E-Mail-Adresse im Kontakt, Impressum und Datenschutz | Eine Adresse |
| `status_we6`, `status_we7`, `status_we8` | Steht statt des Preises, wenn die Wohnung nicht mehr frei ist | `"frei"`, `"reserviert"` oder `"verkauft"` |
| `preis_we6`, `preis_we7`, `preis_we8` | Preis in der Wohnungskarte | So schreiben: `"195.000 €"`. `""` (leer) zeigt „auf Anfrage“ |
| `kleinanzeigen_link` | Link zum Inserat für Wohnung 8, an zwei Stellen | Die Adresse des Inserats. `""` (leer) nimmt den Hinweis raus |

Stehen alle drei Wohnungen auf `"verkauft"`, sagt die Seite das ganz oben, die Preise und der Inserat-Hinweis verschwinden. Der Rest der Seite bleibt.

## 3. Wenn die Seite nach einer Änderung nicht neu wird

Dann hat GitHub die Datei nicht lesen können, meistens wegen eines fehlenden Anführungszeichens. Die alte Seite bleibt so lange online, es geht nichts kaputt. GitHub schickt dir eine Mail mit dem Betreff „Page build failure“.

1. Öffne wieder den Link aus Schritt 1 und schau dir die Zeile an, die du geändert hast. Jeder Wert braucht ein Anführungszeichen vorne und hinten, gerade Anführungszeichen `"`, keine geschwungenen.
2. Korrigiere die Zeile und speichere wieder mit **Commit changes**.
3. Wenn du nicht weiterkommst: Schreib ein Issue unter https://github.com/timimmo/gutshaus-kleinmenow/issues/new mit dem Satz „Seite baut nicht“.

Ob der letzte Bau geklappt hat, siehst du hier: https://github.com/timimmo/gutshaus-kleinmenow/actions. Grüner Haken heißt gut, rotes Kreuz heißt Fehler.

## 4. Einmal im Jahr

- **Domain:** gutshaus-kleinmenow.de läuft über INWX. Prüfen, dass die automatische Verlängerung an ist und die hinterlegte Zahlungsweise noch gilt. Die Einstellungen zur Domain (DNS) nicht anfassen.
- **GitHub-Konto:** Zwei-Faktor-Anmeldung bleibt an, die Wiederherstellungscodes liegen an einem sicheren Ort: https://github.com/settings/security
- **GitHub Pages:** https://github.com/timimmo/gutshaus-kleinmenow/settings/pages öffnen. Bei der Domain muss ein grüner Haken stehen, „Enforce HTTPS“ bleibt angehakt. Steht dort eine gelbe Warnung, ein Issue schreiben.
- **Inhalt:** Einmal durch die Seite lesen. Stimmen Preise und Status? Gilt der Kleinanzeigen-Link noch? Steht noch irgendwo „geplant“, obwohl es inzwischen gebaut ist (Außenküche, Gartenbad, WLAN, Fitnessraum, Steg)? Fährt der RE 5 noch stündlich?
- **Nicht ändern:** Die Datei `CNAME` im Repository und die Einstellung, dass die Seite aus dem Branch `main` gebaut wird. Beides braucht die Domain.

Das Zertifikat für https erneuert GitHub von selbst. Schriften und Bilder liegen alle im Repository, es gibt keine Dienste, die ablaufen oder bezahlt werden müssen, außer der Domain.

## 5. Was nicht in der Datei steht

Für neue Sätze, Fotos, Abschnitte oder eine andere Aufteilung der Seite schreibst du weiter ein Issue: https://github.com/timimmo/gutshaus-kleinmenow/issues/new. Björn schaut dort nur noch ab und zu rein. Rechne also nicht mit einer schnellen Antwort und sammle kleine Wünsche lieber in einem Issue.

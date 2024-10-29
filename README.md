# new.prototypefund.de

Es geht weiter mit dem Prototype Fund! Ab 2025 werden wir 4 Jahrgänge auf dem Weg zum Open-Source-Software-Prototypen begleiten.
Der Bewerbungszeitraum für Jahrgang 1 wird dabei bereits starten, während die 16. Runde noch gefördert wird. Auf dieser Webseite sammeln wir alle Infos, die für Bewerber\*innen der Neuauflage interessant sind.

Die Webseite basiert auf [Hugo](https://gohugo.io/) und dem [Toha-Theme](https://themes.gohugo.io/themes/toha/).


# Deployment

Die Webseite wird nach Veränderungen in diesem Repository automatisch nach [new.prototypefund.de](https://new.prototypefund.de) deployed. Build-Status und eventuelle Fehlermeldungen [finden sich hier](https://lab.okfn.de/build-status/).

# Content

### Texte

Liegen alle unter /data. In /de die Deutschen, in /en die Englischen. Formatiert werden die Texte per [Markdown](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet).
Außerdem gibt es unter /i18n/en.toml bzw. /i18n/de.toml einige Übersetzungen, die vor allen Dingen Bezeichnungen und generische Wörter sind.

Achtung: Die Texte liegen alle in Yaml-Dateien. Daraus ergeben sich einige Besonderheiten: Mehrzeilige Strings (z.B. für mehrere Absätze oder mehrere Aufzählungszeichen als Antwort auf eine Frage) werden mithilfe des `|` und darauf folgendem Einrücken signalisiert, also z.B.:
```
summary: |
  Hier ist der erste Absatz des Textes.

  Hier ist der zweite Absatz des Textes.
url:  test.com
```

Sobald eine Zeile nicht mehr eingerückt ist, wird diese nicht mehr als Wert verstanden, also in obigem Beispiel ist `url: test.com` kein Teil der summary mehr und resultiert, wenn die Seite das Feature unterstützt, in einem Button der zur URL führt. Hingegen:
```
summary: |
  Hier ist der erste Absatz des Textes.

  Hier ist der zweite Absatz des Textes.
  url:  test.com
```
würde dazu führen, dass `url: text.com` in die Summary mit aufgenommen wird.

Ein einfacher Zeilenumbruch ohne Leerzeile wird  mit `\` am Ende signalisiert:
```
summary: |
  Hier ist der erste Absatz des Textes.\
  Hier fängt ein zweiter Absatz an, der jedoch nicht durch eine Leerzeile getrennt ist.
```

### Bilder

Liegen unter /assets/images. .png, .jpg und .svg funktionieren als Formate.
Aufgerufen werden sie dann mit /images/image.svg


# Anpassungen

Viele Custom SCSS und angepasste HTML. z.T. nicht so sauber, work in Progress - funktioniert aber alles.

### Farben

Können in /assets/styles/variables.scss verändert werden - einige Anpassungen funktionieren (visuell) nur, wenn an den richtigen Stellen gleiche Farben genutzt werden.

### Fonts

Liegen in /static/fonts. Werden in /assets/styles/overide.scss eingebunden.

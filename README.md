# new.prototypefund.de

Es geht weiter mit dem Prototype Fund! Ab 2025 werden wir 4 Jahrgänge auf dem Weg zum Open-Source-Software-Prototypen begleiten.
Der Bewerbungszeitraum für Jahrgang 1 wird dabei bereits starten, während die 16. Runde noch gefördert wird. Auf dieser Webseite sammeln wir alle Infos, die für Bewerber\*innen der Neuauflage interessant sind.

Die Webseite basiert auf [Hugo](https://gohugo.io/) und dem [Toha-Theme](https://themes.gohugo.io/themes/toha/).


## Content

#### Texte

Liegen alle unter /data. In /de die Deutschen, in /en die Englischen. Anpassungen einfach per Markdown.
Außerdem gibt es unter /i18n/en.toml bzw. /i18n/de.toml einige Übersetzungen, die vor allen Dingen Bezeichnungen und generische Wörter sind.

#### Bilder

Liegen unter /assets/images. .png, .jpg und .svg funktionieren als Formate.
Aufgerufen werden sie dann mit /images/image.svg


## Anpassungen

Viele Custom SCSS und angepasste HTML. z.T. nicht so sauber, work in Progress - funktioniert aber alles.

#### Farben

Können in /assets/styles/variables.scss verändert werden - einige Anpassungen funktionieren (visuell) nur, wenn an den richtigen Stellen gleiche Farben genutzt werden.

#### Fonts

Liegen in /static/fonts. Werden in /assets/styles/overide.scss eingebunden.

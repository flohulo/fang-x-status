# Fang X Status

<!--start: description-->

Statusseite für [Fang X](https://github.com/flohulo/fang-x): Sie zeigt, ob die App läuft, meldet
Störungen automatisch und informiert über Wartungen und Neuigkeiten.

**Statusseite:** <https://flohulo.github.io/fang-x-status/>

<!--end: description-->

## Live-Status: <!--live status--> wird beim ersten Lauf erzeugt

<!--start: status pages-->
<!--end: status pages-->

## So funktioniert es

- **Prüfung:** Alle 5 Minuten ruft GitHub Actions die App und die Webseite auf.
- **Störungen:** Ist eine Seite nicht erreichbar, legt Upptime automatisch ein Issue an, das als
  Störung auf der Statusseite erscheint. Läuft die Seite wieder, wird das Issue geschlossen.
- **Wartung ankündigen:** Neues Issue mit der Vorlage „Geplante Wartung“ anlegen und Start, Ende
  und betroffene Seiten im Kommentar oben eintragen.
- **Neuigkeit veröffentlichen:** Neues Issue mit der Vorlage „Neuigkeit“ anlegen. Sie erscheint im
  angegebenen Zeitfenster auf der Statusseite.
- **Einstellungen:** Nur [`.upptimerc.yml`](.upptimerc.yml) bearbeiten. Die Workflows in
  `.github/workflows` erzeugt Upptime daraus und überschreibt Änderungen daran.

Die Workflows brauchen das Secret `GH_PAT` (Fine-grained Token für dieses Repo mit Schreibrecht auf
Contents, Issues und Workflows). Die Statusseite wird auf den Branch `gh-pages` gebaut.

<!--start: docs-->
<!--end: docs-->

Betrieben mit [Upptime](https://github.com/upptime/upptime) (MIT-Lizenz, siehe [LICENSE](LICENSE)).

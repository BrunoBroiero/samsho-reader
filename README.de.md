# SamShoAccess

> Übersetzung ohne Prüfung durch einen Muttersprachler. Ein falsches Wort ist ein Fehler, der gemeldet werden sollte.

Barrierefreiheits-Mod für **SAMURAI SHODOWN** (2019, Steam): macht das Spiel mit deinem Screenreader lesbar. Menüs, Optionen, Charakter- und Stage-Auswahl, Untertitel der Story, Tutorial, Befehlsliste, Datenbank, Galerie, Online, Ergebnisse und die Zahlen des Kampfes.

Fast jedes Wort, das du hörst, stammt aus dem Spiel selbst, in der Sprache, auf die es eingestellt ist. Die wenigen Wörter, die das Spiel nicht hat (Richtungen der Befehle, Tastennamen, „Leben“, „Wut“), sind in die elf Sprachen des Spiels übersetzt.

Autor: **Bruno Broiero**. Erstellt mit Claude.

## Voraussetzungen

- SAMURAI SHODOWN für Steam (Windows).
- Ein laufender Screenreader: NVDA oder JAWS. Der Mod spricht über PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), der Mod-Loader für Unreal-Spiele. Er liegt dem Download bei, in der Version, die mit diesem Spiel funktioniert (experimentell, 21. September 2026): nichts muss gesondert geladen werden.
- Ein XInput-Gamepad (Xbox-Art) ist optional, der Mod ist aber darauf ausgelegt.

## Installation

1. Lade die neueste `SamShoAccess-x.y.z.zip` von der Releases-Seite herunter.
2. Entpacke ihren gesamten Inhalt nach `SamuraiShodown\Binaries\Win64\` (der Spielordner; bei Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, den Ordner `ue4ss` und die READMEs.
3. Das Spiel **über Steam** starten (nicht über die .exe: ohne Steam startet es auf Englisch und offline).
4. Beim Laden sagt der Mod „SamShoAccess“. Hörst du es nicht, drücke F8: er nennt den gefundenen Screenreader.

## Tasten des Mods

| Taste | Gamepad | Wirkung |
|---|---|---|
| F1 | Rechter Stick links oder rechts | Sagt alles Festgehaltene (eine Befehlsliste, eine Tabelle, ein Ergebnis) |
| F2 / F3 | Rechter Stick hoch / runter | Vorheriger / nächster Teil des Festgehaltenen |
| F10 | Klick des rechten Sticks | Wechselt die Befehlsnotation (Normal, Arcade, Arcade vereinfacht, FGC, FGC vereinfacht). Die Wahl wird gespeichert |
| F4 | Klick des rechten Sticks, wenn nichts festgehalten ist | Liest die Tastenlegende des Bildschirms („9 oder A Bestätigen, 0 oder B Zurück“) |
| F8 | | Nennt den vom Mod benutzten Screenreader |
| Strg + Esc | | Bringt die Sprache zum Schweigen |

Pfeiltasten, Enter und Rücktaste gehören dem Spiel, nicht dem Mod.

## Im Kampf

Nichts spricht von selbst: den Kampf hört man ohnehin. Mit dem rechten Stick fragst du die gewünschte Zahl ab:

| Rechter Stick | Sagt |
|---|---|
| Links | Leben beider Seiten: „Leben 71%, 80%“ (deine Seite zuerst) |
| Hoch | Wut: „Wut 41%, maximal“ |
| Runter | Gewonnene Runden: „RUNDEN 1, 0“. In Survival, Zeitrennen und Ironman deine Siege in Folge |
| Rechts | Die Rundenzeit |
| Klick | Alles zusammen |

Tastatur: F2 Leben, F3 Wut, F10 Runden, F1 alles.

In Survival, Zeitrennen und Ironman wird nur deine Seite gesagt.

## Die Befehlsliste und ihre Notationen

Im Spiel ist ein Befehl eine Reihe von Bildern: Pfeile, Tasten, ein „Plus“, Bedingungen. Der Mod macht Wörter daraus, und weil Spieler aus verschiedenen Richtungen zu einer Befehlsliste kommen (Spielhalle, Foren oder keins von beiden), bietet er fünf Arten, sie zu sagen. F10 oder der Klick des rechten Sticks wechselt sie, und die Wahl wird gespeichert. Derselbe Befehl, Viertelkreis vorwärts und schwerer Hieb, in jeder:

| Notation | So klingt es |
|---|---|
| Normal | unten, diagonal unten vorwärts, vorwärts plus Schwerer Hieb |
| Arcade | Viertelkreis vorwärts, Schwerer Hieb |
| Arcade vereinfacht | Viertelkreis vorwärts, C |
| FGC | 2 3 6, Schwerer Hieb |
| FGC vereinfacht | 2 3 6, C |

- **Normal** sagt jede Richtung mit ihrem Wort. Die längste, und die, die nichts voraussetzt.
- **Arcade** benennt die Figur: Viertelkreis, Halbkreis, Dragon Punch und ihre Umkehrungen. So sagt man Befehle laut.
- **FGC** nutzt die Ziffern des Nummernblocks, die Notation der Community: 6 ist vorwärts, 2 unten, 3 die Diagonale unten vorwärts; immer nach rechts blickend.
- Die **vereinfachten** Varianten ersetzen die Tastennamen durch die Buchstaben des Automaten: A leichter Hieb, B mittlerer, C schwerer, D Tritt.

Wie das Vorlesen gedacht ist, denn ein Bild sagt mit seiner Form Dinge, die Wörter laut sagen müssen:

- Eine Diagonale ist eine einzige Eingabe, darum heißt sie „diagonal“: „unten, diagonal unten vorwärts, vorwärts“. Als „unten, unten vorwärts, vorwärts“ gesagt, weiß niemand, ob es eine Eingabe ist oder zwei.
- Zwei aneinander gezeichnete Tasten werden zusammen gedrückt, darum verbindet sie in jeder Notation ein „plus“.
- Eine Bedingung, die das Spiel um den Namen des Zugs zeichnet („während ~“), wird einmal gesagt, nicht in zwei Hälften.
- Eine Bedingung wie „wiederholt“ wird nach den Tasten gesagt, für die sie gilt: „vorwärts plus Leichter Hieb, wiederholt“ – so, wie man es sagt, nicht wie es gezeichnet ist.
- Die Namen der Tasten und Bedingungen sind die Wörter des Spiels aus der Legende seiner eigenen Befehlsliste; Richtungen, Figuren, „plus“ und „oder“ sind die des Mods, in den elf Sprachen.
- „Oder“ kommt im Spiel in mehreren Formen vor (zwei Tasten zur Wahl, zwei Befehle, eine Liste); alle werden mit demselben Wort gesagt.

Die Liste wird mit dem rechten Stick durchgegangen (hoch und runter Zug für Zug, links oder rechts ganz) oder mit F2, F3 und F1. Beim Betreten sagt der Mod Kämpfer und Kategorie („SHIKI, SPEZIALZÜGE“), dann jeden Zug als „Name, Bedingung falls vorhanden: Befehl“, zum Beispiel „Elysium Halo: vorwärts, unten, diagonal unten vorwärts plus Leichter Hieb oder Mittlerer Hieb oder Schwerer Hieb“.

## Was gelesen wird

- Hauptmenü und alle Untermenüs, mit der Beschreibung jedes Eintrags.
- Optionen: Spiel, Anzeige, Ton (Lautstärken in %), Sprache und Untertitel, Tastenbelegung (jede Aktion mit ihrer Taste oder ihrem Button).
- Charakterauswahl mit Zufall, Kostümen und Farben; Stage-Auswahl; Seitenzuweisung im Versus.
- Story: Untertitel und Dialoge, Freischaltungen, Epilog und Abspann.
- Tutorial: Anweisung, Aufgabe und Abschlussmeldung, mit den Tasten als Wörtern.
- Befehlsliste: jeder Zug mit seinem Befehl in der gewählten Notation; mit Stick oder F2 / F3 durchgehbar.
- Pause und Trainingseinstellungen.
- Datenbank: Profil, eigene Ranglisten, allgemeine Aufzeichnungen.
- Galerie: Filme, Illustrationen, Stimmen und Musik, mit Reitern und Seiten.
- Online: Bestenlisten, Bildschirme für Rang- und lockere Kämpfe, Geisterlisten des Geisterkampfs.
- Ergebnisse: der Spruch des Siegers wird von selbst gelesen; die Wertung wird festgehalten und mit Stick oder F1 abgefragt.
- Freischaltungsbanner und Hinweise.

## Was nicht gelesen wird

- Der Glückwunschbildschirm am Ende der Story ist ein Bild ohne Text.
- Online-Räume und Chat wurden nicht mit Gegnern getestet.

## Sprachen

Der Mod spricht die Sprache des Spiels. Seine eigenen Wörter wurden nur auf Spanisch nach Gehör geprüft; in den anderen Sprachen sind sie ohne Durchsicht durch einen Sprecher übersetzt. Ein falsches Wort ist ein Fehler, der gemeldet werden sollte.

## Hinweise

- Der Mod verändert keine Spieldatei.
- UE4SS stammt vom RE-UE4SS-Team unter der MIT-Lizenz; `prism.dll` und `tolk.dll` stammen aus [PRISM](https://github.com/ethindp/prism) unter der MPL 2.0. Siehe `THIRD-PARTY.md`.
- Zum Deinstallieren `dwmapi.dll` und den Ordner `ue4ss` löschen.
- Der Quellcode des Mods ist noch nicht öffentlich; das wird er, sobald sich der Mod im Gebrauch eingespielt hat. Der Download ist frei nutzbar.

# SamSho Reader

[English](README.md) · [Español](README.es.md) · **Deutsch** · [Français](README.fr.md) · [Italiano](README.it.md) ·
[Português (Brasil)](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Ein Screenreader-Mod für **SAMURAI SHODOWN** (2019; Steam, PC). Er liest Menüs, Story, Befehlslisten, Tabellen und Bildschirmtext über den Screenreader vor, den du ohnehin benutzt (NVDA, JAWS), in der Sprache, in der das Spiel läuft.

Von Bruno Broiero, mit Hilfe von Claude.

## Was er tut

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

Nicht gelesen wird:

- Der Glückwunschbildschirm am Ende der Story ist ein Bild ohne Text.
- Online-Räume und Chat wurden nicht mit Gegnern getestet.

## Installation

Du brauchst die Steam-PC-Version von SAMURAI SHODOWN, Windows x64 und einen laufenden Screenreader (NVDA oder JAWS). UE4SS, der Mod-Loader für Unreal-Spiele, liegt dem Zip bei, in der Version, die mit diesem Spiel funktioniert.

Entpacke den gesamten Inhalt des Zips nach `SamuraiShodown\Binaries\Win64` (bei Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, den Ordner `ue4ss` und diese READMEs.

Starte das Spiel über Steam, nicht über die .exe: ohne Steam startet es auf Englisch und offline. Der Mod sagt „SamSho Reader“, sobald er läuft; hörst du es nicht, nennt F8 den gefundenen Screenreader. Keine Spieldatei wird verändert.

Zum Deinstallieren `dwmapi.dll` und den Ordner `ue4ss` löschen. UE4SS und PRISM, die Bibliothek, die mit dem Screenreader spricht, stehen unter eigenen Lizenzen: siehe `THIRD-PARTY.md`.

## Tasten

Außerhalb eines Kampfes:

| Taste | Gamepad | Wirkung |
|---|---|---|
| F1 | Rechter Stick links oder rechts | Sagt alles Festgehaltene (eine Befehlsliste, eine Tabelle, ein Ergebnis) |
| F2 / F3 | Rechter Stick hoch / runter | Vorheriger / nächster Teil des Festgehaltenen |
| F10 | Klick des rechten Sticks | Wechselt die Befehlsnotation (Normal, Arcade, Arcade vereinfacht, FGC, FGC vereinfacht). Die Wahl wird gespeichert |
| F4 | Klick des rechten Sticks, wenn nichts festgehalten ist | Liest die Tastenlegende des Bildschirms („9 oder A Bestätigen, 0 oder B Zurück“) |

In einem Kampf:

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

Immer:

| Taste | Gamepad | Wirkung |
|---|---|---|
| F6 | L3 + R3 (beide Sticks zugleich gedrückt) | Schaltet den Mod aus und wieder ein, bestätigt mit den Wörtern des Spiels für an und aus. Wird nicht gespeichert: er startet immer eingeschaltet |
| F8 | | Nennt den vom Mod benutzten Screenreader |

## Was F1, F2, F3 und der rechte Stick lesen

Viele Bildschirme zeigen mehr als das, was unter dem Cursor liegt: eine Befehlsliste, die Punkte eines Ergebnisses, eine Tabelle mit Rekorden, eine Lektion. Der Mod liest das beim Ankommen nicht alles vor: er behält es und gibt es über diese Tasten heraus: F3 geht zum nächsten Stück, F2 zurück zum vorigen, F1 sagt alles auf einmal. Am Ende sagt F3 nichts: daran erkennst du, dass nichts mehr kommt. Am Pad macht der rechte Stick dasselbe: unten ist F3, oben F2, links oder rechts F1.

Was ein Stück ist, hängt vom Bildschirm ab:

- **Befehlsliste**: jeder Move mit seiner Eingabe, in der mit F10 oder dem Stick-Klick gewählten Notation; beim Wechsel wird der Move in der neuen wiederholt. Beim Betreten werden Kämpfer und Kategorie gesagt.
- **Tutorial**: jeder Satz der Erklärung und der Aufgabe, mit den Eingaben in Worten; der Klick wechselt auch hier die Notation.
- **Ergebnis** nach einem Kampf: der Satz des Siegers wird von selbst gesagt; die Punkte warten in den Tasten, mit Absicht, damit der Satz nicht unter Zahlen begraben wird.
- **Versus-Ergebnis**: Siege, Niederlagen, Unentschieden, Quote und Punkte jeder Seite.
- **Spielerdaten**: die Tabellen mit Rekorden und Ranglisten, eine Zeile pro Stück; beim Ankommen werden Titel und erste Zeile gesagt.
- **Tastenlegende**: ist nichts behalten, liest der Stick-Klick (oder F4) die Tastenlegende des Bildschirms selbst.

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

## Ein Problem melden

Beende das Spiel normal und schicke `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log`: darin steht, was das Spiel gezeigt und was der Mod dazu gesagt hat, im genauen Wortlaut, du musst also nichts mitschreiben. Nenne den Bildschirm und was du zu hören erwartet hast.

## Bauen

Der Mod ist Lua, geladen von UE4SS; kompiliert wird nur `prism_bridge.dll`, das kleine native Modul, das die Sprache an PRISM übergibt und das Pad liest (`native\prism_bridge\build.ps1`, braucht MSVC). `python tools\package.py` baut das Release-Zip aus dem Spielordner.

## Übersetzungen

Dieses README erscheint in jeder Sprache, die das Spiel unterstützt. Nur die englische und die spanische Fassung wurden von einem Sprecher geprüft; Korrekturen an den übrigen sind willkommen. Der Mod selbst spricht die Sprache des Spiels: fast alles, was er sagt, ist der Text des Spiels, und seine wenigen eigenen Wörter (Richtungen, Tastennamen, „Leben“, „Wut“) wurden nur auf Spanisch nach Gehör geprüft.

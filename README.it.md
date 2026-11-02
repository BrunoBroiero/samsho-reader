# SamSho Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · **Italiano** ·
[Português (Brasil)](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Un mod per screen reader per **SAMURAI SHODOWN** (2019; Steam, PC). Legge i menu, la storia, le liste di comandi, le tabelle e il testo a schermo con lo screen reader che già usi (NVDA, JAWS), nella lingua in cui gira il gioco.

Di Bruno Broiero, con l'aiuto di Claude.

## Cosa fa

- Il menu principale e tutti i sottomenu, con la descrizione di ogni voce.
- Opzioni: gioco, schermo, audio (volumi in %), lingua e sottotitoli, configurazione dei pulsanti (ogni azione con il suo tasto o pulsante).
- Selezione del personaggio, compresi casuale, costumi e colori; selezione dello stage; assegnazione dei lati in Versus.
- Storia: sottotitoli e dialoghi, sblocchi, epilogo e titoli di coda.
- Tutorial: istruzione, compito e messaggio finale, con i tasti in parole.
- Lista dei comandi: ogni mossa con il suo comando nella notazione scelta; scorsa con lo stick o F2 / F3.
- Pausa e impostazioni dell'Allenamento.
- Database: profilo, classifiche personali, registri generali.
- Galleria: filmati, illustrazioni, voci e musica, con le loro schede e pagine.
- Online: classifiche, schermate di battaglia classificata e casual, liste dei fantasmi della Battaglia fantasma.
- Risultati: la frase del vincitore viene letta da sola; il punteggio resta trattenuto e si chiede con lo stick o F1.
- Avvisi di sblocco e notifiche.

Non viene letto:

- La schermata di congratulazioni alla fine della storia è un'immagine senza testo.
- Le stanze e la chat online non sono state provate con avversari.

## Installazione

Servono la versione Steam per PC di SAMURAI SHODOWN, Windows x64 e uno screen reader in esecuzione (NVDA o JAWS). UE4SS, il caricatore di mod per i giochi Unreal, è incluso nello zip, nella versione che funziona con questo gioco.

Estrai tutto il contenuto dello zip in `SamuraiShodown\Binaries\Win64` (su Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, la cartella `ue4ss` e questi README.

Avvia il gioco da Steam, non dal .exe: senza Steam parte in inglese e offline. Il mod dice "SamSho Reader" appena è in funzione; se non lo senti, F8 dice il nome dello screen reader trovato. Nessun file del gioco viene modificato.

Per disinstallare, elimina `dwmapi.dll` e la cartella `ue4ss`. UE4SS e PRISM, la libreria che parla con lo screen reader, hanno le proprie licenze: vedi `THIRD-PARTY.md`.

## Tasti

Fuori da un incontro:

| Tasto | Gamepad | Cosa fa |
|---|---|---|
| F1 | Stick destro sinistra o destra | Dice tutto ciò che è trattenuto (una lista di comandi, una tabella, un risultato) |
| F2 / F3 | Stick destro su / giù | Elemento precedente / successivo di ciò che è trattenuto |
| F10 | Clic dello stick destro | Cambia la notazione dei comandi (Normale, Arcade, Arcade semplificata, FGC, FGC semplificata). La scelta viene salvata |
| F4 | Clic dello stick destro, quando non c'è nulla trattenuto | Legge la legenda dei pulsanti della schermata ("9 o A Conferma, 0 o B Indietro") |

In un incontro:

Nulla parla da solo: il combattimento si sente già. Con lo stick destro chiedi il dato che ti serve:

| Stick destro | Dice |
|---|---|
| Sinistra | Vita di entrambi i lati: "vita 71%, 80%" (prima il tuo lato) |
| Su | Furia: "furia 41%, massima" |
| Giù | Round vinti: "ROUND 1, 0". In Sopravvivenza, Prova a tempo e Ironman, le tue vittorie consecutive |
| Destra | Il tempo del round |
| Clic | Tutto insieme |

Tastiera: F2 vita, F3 furia, F10 round, F1 tutto.

In Sopravvivenza, Prova a tempo e Ironman viene detto solo il tuo lato.

Sempre:

| Tasto | Gamepad | Cosa fa |
|---|---|---|
| F6 | L3 + R3 (le due levette premute insieme) | Spegne il mod e lo riaccende; lo conferma con le parole del gioco per attivato e disattivato. Non viene salvato: parte sempre acceso |
| F8 | | Dice quale screen reader usa il mod |

## Cosa leggono F1, F2, F3 e lo stick destro

Molte schermate mostrano più di ciò che sta sotto il cursore: una lista di comandi, i punteggi di un risultato, una tabella di record, una lezione. Il mod non legge tutto all'arrivo: lo conserva e lo consegna con questi tasti: F3 passa al pezzo successivo, F2 torna al precedente e F1 dice tutto in una volta. Alla fine F3 non dice nulla: così si sa che non c'è altro. Sul pad, la levetta destra fa lo stesso: giù è F3, su è F2, sinistra o destra è F1.

Cosa sia un pezzo dipende dalla schermata:

- **Lista di comandi**: ogni mossa con il suo comando, nella notazione scelta con F10 o il clic della levetta; cambiandola, la mossa viene ripetuta nella nuova. Entrando si dicono il personaggio e la categoria.
- **Tutorial**: ogni frase della spiegazione e del compito, con gli input messi in parole; il clic ne cambia anche la notazione.
- **Risultato**, a fine incontro: la frase del vincitore viene detta da sola; i punteggi aspettano nei tasti, apposta, perché la frase non resti sepolta sotto le cifre.
- **Risultato del versus**: vittorie, sconfitte, pareggi, percentuale e punti di ciascun lato.
- **Dati giocatore**: le tabelle di record e classifiche, una riga per pezzo; all'arrivo si dicono il titolo e la prima riga.
- **Legenda dei pulsanti**: senza nulla di conservato, il clic della levetta (o F4) legge la legenda dei pulsanti della schermata stessa.

## La lista dei comandi e le sue notazioni

Nel gioco un comando è una fila di disegni: frecce, pulsanti, un "più", condizioni. Il mod li trasforma in parole e, poiché ogni giocatore arriva a una lista di comandi da un posto diverso (la sala giochi, i forum, o nessuno dei due), offre cinque modi di dirli. Si cambia con F10 o con il clic dello stick destro, e la scelta viene salvata. Lo stesso comando, quarto di cerchio avanti e taglio forte, in ognuna:

| Notazione | Come suona |
|---|---|
| Normale | giù, diagonale giù avanti, avanti più Taglio forte |
| Arcade | quarto di cerchio avanti, Taglio forte |
| Arcade semplificata | quarto di cerchio avanti, C |
| FGC | 2 3 6, Taglio forte |
| FGC semplificata | 2 3 6, C |

- **Normale** dice ogni direzione con la sua parola. La più lunga, e quella che non dà nulla per scontato.
- **Arcade** nomina la figura: quarto di cerchio, mezzo cerchio, dragon punch e i loro inversi. È come si dicono i comandi a voce.
- **FGC** usa i numeri del tastierino numerico, la notazione della community: 6 è avanti, 2 giù, 3 la diagonale giù avanti; sempre rivolti a destra.
- Le varianti **semplificate** sostituiscono i nomi dei pulsanti con le lettere del cabinato: A taglio leggero, B medio, C forte, D calcio.

Come è stata pensata la lettura, perché un disegno dice con la forma cose che le parole devono dire ad alta voce:

- Una diagonale è un solo input, quindi si chiama "diagonale": "giù, diagonale giù avanti, avanti". Detto "giù, giù avanti, avanti" non si capisce se sono due input o uno.
- Due pulsanti disegnati attaccati si premono insieme, quindi sono uniti da "più" in tutte le notazioni.
- Una condizione che il gioco disegna attorno al nome della mossa ("durante ~") si dice una volta sola, non in due metà.
- Una condizione come "ripetutamente" si dice dopo i pulsanti a cui si riferisce: "avanti più Taglio leggero, ripetutamente" - come si dice, non come è disegnato.
- I nomi dei pulsanti e delle condizioni sono le parole del gioco, prese dalla legenda della sua stessa lista dei comandi; direzioni, figure, "più" e "o" sono del mod, nelle undici lingue.
- "O" ha diverse forme nel gioco (due pulsanti alternativi, due comandi, un elenco); tutte si dicono con la stessa parola.

La lista si scorre con lo stick destro (su e giù, mossa per mossa; sinistra o destra, tutta) o con F2, F3 e F1. Entrando dice il lottatore e la categoria ("SHIKI, MOSSE SPECIALI"), poi ogni mossa come "nome, condizione se c'è: comando", per esempio "Elysium Halo: avanti, giù, diagonale giù avanti più Taglio leggero o Taglio medio o Taglio forte".

## Segnalare un problema

Chiudi il gioco normalmente e invia `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log`: registra ciò che il gioco ha mostrato e ciò che il mod ne ha detto, parola per parola, quindi non serve annotare ciò che hai sentito. Indica la schermata e cosa ti aspettavi di sentire.

## Compilazione

Il mod è in Lua, caricato da UE4SS; non si compila nulla tranne `prism_bridge.dll`, il piccolo modulo nativo che passa la voce a PRISM e legge il pad (`native\prism_bridge\build.ps1`, richiede MSVC). `python tools\package.py` costruisce lo zip della release dalla cartella del gioco.

## Traduzioni

Questo README esce in tutte le lingue supportate dal gioco. Solo le versioni inglese e spagnola sono state riviste da un parlante; le correzioni alle altre sono benvenute. Il mod stesso parla la lingua del gioco: quasi tutto ciò che dice è testo del gioco, e le sue poche parole proprie (direzioni, nomi dei tasti, "vita", "rabbia") sono state verificate a orecchio solo in spagnolo.

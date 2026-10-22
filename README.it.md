# SamShoAccess

> Traduzione non revisionata da un madrelingua. Una parola sbagliata è un errore che vale la pena segnalare.

Mod di accessibilità per **SAMURAI SHODOWN** (2019, Steam): rende il gioco leggibile con il tuo screen reader. Menu, opzioni, selezione del personaggio e dello stage, sottotitoli della storia, tutorial, lista dei comandi, database, galleria, online, risultati e i numeri del combattimento.

Quasi tutte le parole che sentirai sono quelle del gioco, nella lingua in cui è impostato. Le poche parole che il gioco non ha (direzioni dei comandi, nomi dei tasti, "vita", "furia") sono tradotte nelle undici lingue del gioco.

Autore: **Bruno Broiero**. Realizzato con Claude.

## Requisiti

- SAMURAI SHODOWN per Steam (Windows).
- Uno screen reader in esecuzione: NVDA o JAWS. Il mod parla tramite PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), il caricatore di mod per i giochi Unreal. È incluso nel download, nella versione che funziona con questo gioco (sperimentale, 21 settembre 2026): non c'è nulla da scaricare a parte.
- Un gamepad XInput (tipo Xbox) è facoltativo, ma il mod è pensato per quello.

## Installazione

1. Scarica l'ultimo `SamShoAccess-x.y.z.zip` dalla pagina Releases.
2. Estrai tutto il contenuto in `SamuraiShodown\Binaries\Win64\` (la cartella del gioco; su Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, la cartella `ue4ss` e i README.
3. Avvia il gioco **da Steam** (non dal .exe: senza Steam parte in inglese e offline).
4. Al caricamento il mod dice "SamShoAccess". Se non lo senti, premi F8: dice il nome dello screen reader trovato.

## Tasti del mod

| Tasto | Gamepad | Cosa fa |
|---|---|---|
| F1 | Stick destro sinistra o destra | Dice tutto ciò che è trattenuto (una lista di comandi, una tabella, un risultato) |
| F2 / F3 | Stick destro su / giù | Elemento precedente / successivo di ciò che è trattenuto |
| F10 | Clic dello stick destro | Cambia la notazione dei comandi (Normale, Arcade, Arcade semplificata, FGC, FGC semplificata). La scelta viene salvata |
| F4 | Clic dello stick destro, quando non c'è nulla trattenuto | Legge la legenda dei pulsanti della schermata ("9 o A Conferma, 0 o B Indietro") |
| F8 | | Dice quale screen reader usa il mod |
| Ctrl + Esc | | Zittisce la voce |

Le frecce, Invio e Backspace sono del gioco, non del mod.

## Durante il combattimento

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

## Cosa viene letto

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

## Cosa non viene letto

- La schermata di congratulazioni alla fine della storia è un'immagine senza testo.
- Le stanze e la chat online non sono state provate con avversari.

## Lingue

Il mod parla nella lingua del gioco. Le parole proprie del mod sono state verificate a orecchio solo in spagnolo; nelle altre lingue sono tradotte senza la revisione di un parlante. Una parola sbagliata è un errore che vale la pena segnalare.

## Note

- Il mod non modifica alcun file del gioco.
- UE4SS è del team RE-UE4SS, con licenza MIT; `prism.dll` e `tolk.dll` provengono da [PRISM](https://github.com/ethindp/prism), con licenza MPL 2.0. Vedi `THIRD-PARTY.md`.
- Per disinstallare, elimina `dwmapi.dll` e la cartella `ue4ss`.
- Il codice sorgente del mod non è ancora pubblico; lo sarà quando il mod si sarà assestato con l'uso. Il download è libero da usare.

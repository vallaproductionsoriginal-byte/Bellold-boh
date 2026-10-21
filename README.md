# Bellold-boh

Un plugin di **Valla Productions**, creato da **Francesco Valla**.

Riverbero gratuito VST3 per Windows x64 e VST3/Audio Unit per macOS Apple Silicon,
con 22 modalità, tre epoche sonore, preset e interfaccia ridimensionabile con tema chiaro e scuro.

![Interfaccia di Bellold-boh](images/Bellold-boh.png)

## Download

[Scarica l'ultima release](https://github.com/vallaproductionsoriginal-byte/Bellold-boh/releases/latest)
e scegli il pacchetto per il tuo sistema:

- **Bellold-boh-1.0.0-mac-arm64.zip**: VST3 e Audio Unit per Mac Apple Silicon.
- **Bellold-boh-1.0.0-win-x64.zip**: VST3 per Windows a 64 bit.

Il plugin viene distribuito in formato binario. Il repository contiene la
documentazione, le licenze e l'immagine dell'interfaccia.

## Requisiti macOS

- Mac con processore Apple Silicon (arm64).
- macOS 11 o successivo. La build richiede almeno macOS 11; la release è stata
  verificata sul Mac di sviluppo, senza prove su ogni versione di macOS.
- Una DAW con supporto VST3 o Audio Unit, eseguita nativamente su Apple Silicon.
- Per Logic Pro usa il formato Audio Unit (`Bellold-boh.component`).

## Installazione macOS

Non serve compilare nulla né installare strumenti per sviluppatori.
Bellold-boh è un effetto da usare nella tua DAW (il programma con cui fai musica).

1. Chiudi la DAW, scarica **Bellold-boh-1.0.0-mac-arm64.zip** dalle
   [release ufficiali](https://github.com/vallaproductionsoriginal-byte/Bellold-boh/releases/latest)
   e fai doppio clic sullo ZIP per estrarlo.
2. In Finder scegli **Vai → Vai alla cartella…** (`⇧⌘G`), incolla il percorso
   del formato che vuoi usare e premi Invio:
   - **VST3:** `~/Library/Audio/Plug-Ins/VST3/`.
   - **Audio Unit / Logic Pro:** `~/Library/Audio/Plug-Ins/Components/`.
   Il simbolo `~` indica la tua cartella utente. Se la cartella manca, apri
   `~/Library/Audio/Plug-Ins/` e creala con **File → Nuova cartella**, chiamandola
   `VST3` oppure `Components`.
3. Dalla cartella estratta copia **Bellold-boh.vst3** nella cartella `VST3`
   oppure **Bellold-boh.component** nella cartella `Components`. Puoi installare
   entrambi. Mantieni intero ciascun file/cartella, compreso il suo contenuto.
4. Apri la DAW ed esegui una nuova scansione dei plugin se necessario.
5. Cerca **Bellold-boh**, produttore **Valla Productions**, categoria **Reverb**.
   In Logic Pro appare nello slot degli effetti audio, sotto
   **Audio Units → Valla Productions**.

I file `.vst3` e `.component` vengono caricati dalla DAW: il doppio clic in Finder
non serve ad avviare Bellold-boh come applicazione autonoma.

### Se macOS blocca il plugin perché lo sviluppatore non è verificato

Bellold-boh **non è firmato con un certificato Apple Developer ID e non è
notarizzato da Apple**. Usa una firma locale detta *ad hoc*, che non identifica
lo sviluppatore per Apple. Al primo caricamento macOS può quindi mostrare
«impossibile verificare lo sviluppatore» o «Apple non può verificare la presenza
di software dannoso».

Procedi con l'autorizzazione solo per la copia scaricata dalle release ufficiali
di questo repository e se ti fidi della sua provenienza.

1. Avvia la DAW e lascia che provi a caricare/scansionare Bellold-boh. Se compare
   l'avviso, chiudilo con **Annulla** o **Fine**.
2. Apri **menu Apple  → Impostazioni di Sistema → Privacy e sicurezza**
   e scorri fino alla sezione **Sicurezza**. Su macOS 11 e 12 il percorso è
   **Preferenze di Sistema → Sicurezza e Privacy → Generali**.
3. Se compare un messaggio relativo a **Bellold-boh**, premi **Apri comunque**
   e conferma con la password del Mac o Touch ID, se richiesto.
4. Conferma **Apri** nell'eventuale avviso successivo, poi riavvia la DAW
   e ripeti la scansione.

La procedura è descritta anche nella
[guida ufficiale Apple](https://support.apple.com/it-it/102445).

### Se «Apri comunque» non compare o il plugin resta bloccato

Per i plugin caricati dentro una DAW il pulsante può non comparire. Puoi rimuovere
il contrassegno di quarantena del download dalla sola copia di Bellold-boh
installata al passaggio 3:

1. Chiudi la DAW.
2. Premi `⌘Spazio`, cerca **Terminale** e aprilo.
3. Copia e incolla il comando per il formato installato, poi premi Invio.
   Se hai installato entrambi i formati, esegui entrambi i comandi, uno alla volta.

**Audio Unit / Logic Pro:**

```bash
xattr -dr com.apple.quarantine "$HOME/Library/Audio/Plug-Ins/Components/Bellold-boh.component"
```

**VST3:**

```bash
xattr -dr com.apple.quarantine "$HOME/Library/Audio/Plug-Ins/VST3/Bellold-boh.vst3"
```

I comandi agiscono soltanto sul plugin indicato e sul suo contenuto. Se il
Terminale torna alla riga di comando senza messaggi, l'operazione è terminata.
Se compare **No such file**, verifica di avere copiato il formato giusto nella
cartella indicata. **No such xattr** indica che il contrassegno è già assente.

Riapri la DAW e ripeti la scansione. In Logic Pro apri **Logic Pro → Impostazioni
(o Preferenze) → Gestione plug-in**, seleziona **Bellold-boh** e premi
**Ripristina e scansiona di nuovo la selezione** (*Reset & Rescan Selection*).
Se il plugin non appare nell'elenco, riavvia il Mac e riapri Logic Pro. Vedi anche
la [guida Apple per i plugin non rilevati](https://support.apple.com/en-gb/122179).

Se resta un errore, segnala il testo esatto dell'avviso, la versione di macOS
e la DAW usata nella sezione [Supporto](#supporto).

## Windows x64

Richiede Windows 10 o successivo, processore x64 e una DAW a 64 bit con supporto VST3.
Richiede anche [Microsoft Visual C++ Redistributable x64](https://aka.ms/vc14/vc_redist.x64.exe).

1. Estrai **Bellold-boh-1.0.0-win-x64.zip**.
2. Copia l'intera cartella **Bellold-boh.vst3** in `C:\Program Files\Common Files\VST3\`.
3. Riavvia la DAW o esegui una nuova scansione dei plugin.
4. Cerca **Bellold-boh**, produttore **Valla Productions**, categoria **Reverb**.

Mantieni intatta la cartella `.vst3`, inclusi `Contents` e tutte le sottocartelle.

## Controlli

Mix, predelay, decay, size, attack, damping dei bassi e degli alti, diffusione
early/late, modulazione, low/high cut e larghezza stereo. Le epoche disponibili
sono **1970s**, **1980s** e **NOW**.

Sono inclusi 22 preset. SAVE/LOAD gestiscono i file `.belloldpreset`; COPY/PASTE
trasferiscono i preset tramite appunti. MIX LOCK mantiene il mix quando richiami
un preset. Doppio clic sui controlli per ripristinare il valore iniziale;
clic sul valore per digitarlo. Sono supportati mono e stereo.

## Licenza

Creatore: **Francesco Valla**. Copyright (c) 2026 Francesco Valla.

I componenti originali di Bellold-boh e la documentazione sono soggetti alla
[licenza proprietaria](LICENSE). Tutti i diritti sono riservati; l'uso richiede
l'autorizzazione espressa del titolare nei limiti concessi. Questa distribuzione
non include il codice sorgente del plugin.

JUCE è utilizzato secondo la licenza commerciale **JUCE Starter**. JUCE e le
altre dipendenze conservano le proprie licenze, riportate integralmente dove
necessario in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). La licenza di
Bellold-boh non rilicenzia questi componenti.

## Supporto

Per segnalare problemi, apri una
[issue](https://github.com/vallaproductionsoriginal-byte/Bellold-boh/issues)
indicando sistema operativo, DAW e versione del plugin.

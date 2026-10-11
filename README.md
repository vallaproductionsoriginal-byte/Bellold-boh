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

1. Estrai l'archivio ZIP: contiene entrambi i formati.
2. In Finder scegli **Vai → Vai alla cartella…** e apri la cartella del formato:
   - **VST3:** `~/Library/Audio/Plug-Ins/VST3/`.
   - **Audio Unit / Logic Pro:** `~/Library/Audio/Plug-Ins/Components/`.
   Crea la cartella se manca.
3. Copia il bundle completo **Bellold-boh.vst3** nella cartella VST3 oppure
   **Bellold-boh.component** nella cartella Components. Puoi installare entrambi.
4. Riavvia la DAW o esegui una nuova scansione dei plugin.
5. Cerca **Bellold-boh**, produttore **Valla Productions**, categoria **Reverb**.
   In Logic Pro appare tra gli effetti **Audio Units → Valla Productions**.

I bundle sono firmati ad hoc e non sono notarizzati da Apple. macOS può richiedere
un'autorizzazione in **Impostazioni di Sistema → Privacy e Sicurezza** prima
del caricamento.

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

I componenti originali di Bellold-boh e la documentazione sono concessi sotto
[licenza MIT](LICENSE). Questa distribuzione non include il codice sorgente
del plugin.

JUCE è utilizzato secondo la licenza commerciale **JUCE Starter**. JUCE e le
altre dipendenze conservano le proprie licenze, riportate integralmente dove
necessario in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). La MIT di
Bellold-boh non rilicenzia questi componenti.

## Supporto

Per segnalare problemi, apri una
[issue](https://github.com/vallaproductionsoriginal-byte/Bellold-boh/issues)
indicando sistema operativo, DAW e versione del plugin.

Arile 2026
attualmente sono usciti modelli con contesto (finalmente ) importante, intorno a 1 milione per cominciare a ragionare nella stessa istanza, senza troppe complicazioni
RAG ecc, come naturalezza da parte del tenere traccia da parte del modello di per se, anche via CLI terminale semplice chiamando ollama run ecc, si
avverte la differenza.

Per chi come me ha un po di hardware a dispozisione, sto testando con GPU 3060 la possibilità di sfruttare al max questo vecchio HW ( non in paragone coi bigger )
ma per vedere fino a quanto sia possibile spingere oltre un setup decente.

anche se le macchine stesse raccontano di stare comode con contesti da 16k - 32k, non è vero per niente, io testanto in hermes-agent ( il framework di nousresearch )
istallato localmente in docker anche, non ho potuto credere che a 1/2 della procedura di istallazione verso una macchina esterna, tramite ssh ecc,
abbia perduto il senso del progetto solo perchè per motivi di velocità di risposta in chat, ho dovuto settare a 32k il contesto del modello.

Quando parlo di questo contesto non mi riferisco a tutte le seghe derivanti dal calcolo token:
```
⚙️  /usage
  📊 Session Token Usage
  ────────────────────────────────────────
  Model:                     gemma4:e4b
  Input tokens:                 413,637
  Cache read tokens:                  0
  Cache write tokens:                 0
  Output tokens:                 11,246
  Prompt tokens (total):        413,637
  Completion tokens:             11,246
  Total tokens:                 424,883
  API calls:                         20
  Session duration:              1h 55m
  Cost status:                 unknown
  Cost source:                    none
  Total cost:                     n/a
  ────────────────────────────────────────
  Current context:  25,342 / 131,072 (19%)
  Messages:         42
  Compressions:     0
  Note:             Pricing unknown for gemma4:e4b ```

Mi riferisco a questo : ``` qwen3.6:35b-a3b │ 17.7K/262.1K │ [█░░░░░░░░░] 7% │ 4h 14m``` che,
è esattamente la capacità totale durante le inferenze in chat continua, prima del compact ecc, che se ha un numero 250k e su è qualcosa che funziona, altrimenti NO!

La mia scommessa è tramite un principio di funzionamento a 32k minimo, ( usando una sola GPU 3060 e un modello molto buono in tools ecc gemma4:e4b ) non ottimo come qwen5.5 o 3.6,
riuscire a gestire la programmazione della Vllm definitiva per massimo controllo su 6GPU.

Non sapendo come fare io personalmente sto sfruttando le minime capacità del framework per arrivare a ottimizzare.

Piacere se mi hai letto fin qui, piacere di ricevere aiuto, piacere di dari qualche dritta.
Grazie
P

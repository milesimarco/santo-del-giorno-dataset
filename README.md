# 📅 Santi del Giorno

Dataset open-source dei **santi del giorno** secondo il calendario liturgico cattolico (tradizione italiana).  
I dati sono forniti in formato **JSON**, uno per ogni giorno dell’anno.

## 📖 Descrizione

Questo repository contiene un elenco strutturato dei santi e delle feste liturgiche giorno per giorno.  
Può essere usato per:

- Siti web o blog religiosi/culturali  
- Applicazioni mobile (“Santo del giorno”)  
- Bot Telegram o skill per assistenti vocali  
- Ricerca o studio del calendario liturgico  

> ⚠️ Nota bene: l’elenco è basato principalmente sulla tradizione **italiana**. Alcuni santi e feste sono **universali** (presenti nel Calendario Romano Generale), altri invece sono **locali** o particolarmente venerati in Italia.

## 📂 Struttura del dataset

Ogni record è un oggetto JSON con i seguenti campi:

```json
{
  "giorno": "04-25",
  "santo": "San Marco Evangelista"
}
```

- `giorno`: data in formato `MM-DD`  
- `santo`: santo o ricorrenza principale del giorno  

## 🚀 Installazione / Come usare

Clona il repository:

```bash
git clone https://github.com/milesimarco/santo-del-giorno-dataset.git
cd santi-del-giorno
```

### Node.js (esempio rapido)
```js
// require('./saints_v1.json') se usi CommonJS
import santi from './saints_v1.json' assert { type: 'json' };

const giorno = "04-25";
const santo = santi.find(s => s.giorno === giorno);
console.log(santo?.santo); // San Marco Evangelista
```

### Python
```python
import json
with open("saints_v1.json", "r", encoding="utf-8") as f:
    santi = json.load(f)

giorno = "04-25"
santo = next((s for s in santi if s["giorno"] == giorno), None)
print(santo["santo"] if santo else "Nessun santo trovato")
```

## 📜 Licenza

Puoi utilizzare questo dataset con licenza **MIT** o **CC-BY 4.0** (open data).

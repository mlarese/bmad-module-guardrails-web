# Roster e confini del collegio

Chi entra e su quale segnale. Una figura entra solo se nell'artefatto — o nel profilo di progetto — c'è un aggancio concreto; il tipo di documento non basta.

| Figura | Skill | Entra quando compare |
| ------ | ----- | -------------------- |
| Iris 👁️ | `grl-agent-ui-critic` | markup, CSS, screenshot, design system, landing o pagine viste dall'utente |
| Nora 🔎 | `grl-agent-seo` | pagine indicizzabili e loro struttura, title e meta, URL e redirect, sitemap e robots.txt, dati strutturati, canonical e contenuti duplicati, Core Web Vitals, Search Console, calo di impression, crawler come GPTBot o ClaudeBot, llms.txt e AI Overviews |

Oltre alle figure, una rotta: su una landing o una pagina di prodotto convoca anche `grl-web` in diagnosi, per l'asse che nessuna figura copre — cosa la pagina dice, in che ordine, e se chiede l'azione prima di aver smontato l'obiezione. Quando la pagina arriva dal gate di `grl-web`, la lettura non ripete l'asse ma lo **verifica**: si ricostruisce il brief dalla pagina a freddo e si dice dove diverge da quello scritto. Se non diverge, è una riga sola. Conta come rotta, non come figura del collegio.

## Confini

Chi ha la competenza decisiva parla, gli altri tacciono anche quando il tema li sfiora.

| Questione | Parla | Tace |
| --------- | ----- | ---- |
| Accessibilità WCAG | Nils (l'obbligo) | Iris solo su come realizzarla senza imbruttire |
| Un componente è brutto o generico | Iris | tutti gli altri |
| Una pagina non si trova: domanda di ricerca, indicizzazione, struttura dei contenuti, dati strutturati | Nora | Iris, che parla di come appare; `grl-web`, che parla di cosa argomenta |
| Core Web Vitals | Nora (l'effetto in Search e la soglia) | Bruno se la causa è server, cache o CDN; Iris se è un'immagine o un font della pagina |
| Crawler di modelli linguistici, llms.txt, citazioni in AI Overviews | Nora | Enzo, che resta sull'impianto delle applicazioni AI |
| Una landing non converte: promessa, obiezione, prova, ordine dei blocchi | `grl-web` | Iris, che parla solo di come appare |

Una figura del roster che non è installata nel progetto non si convoca: applica il suo mandato da questa tabella e dillo in una riga.

## Figure fuori da questo modulo

Le tabelle qui sopra citano anche figure Guardrails che questo modulo non installa.
Qui sono installate: Iris (grl-agent-ui-critic), Nora (grl-agent-seo).

Quando il tema appartiene a una figura assente, il confine resta valido: **dichiara che
il tema esce dal perimetro, nomina la competenza che servirebbe e prosegui su ciò che
resta.** Non improvvisare il parere della figura mancante e non fermare il lavoro. Il
modulo che la contiene si installa a parte; il bundle completo `grl` le contiene tutte.

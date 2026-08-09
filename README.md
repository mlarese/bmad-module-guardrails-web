# Guardrails Web Experience (`grw`)

Tre figure di presidio su qualità visiva dell'interfaccia, SEO e media buying/ADV, più i workflow che costruiscono landing page e siti e coordinano audit, piano, tracking e preflight delle campagne Google Ads. Contro le pagine che sembrano generate, le promesse di ranking e la spesa senza misura.

Modulo BMad. È una porzione del bundle [Guardrails](https://github.com/mlarese/bmad-module-guardrails):
stesse figure, stesso comportamento, solo l'area web experience.

> **Generato.** Questo repository è prodotto da `tools/build_modules.py` nel
> repository [bmad-module-guardrails](https://github.com/mlarese/bmad-module-guardrails).
> Le modifiche si fanno lì e poi si rigenera: qui vengono sovrascritte.

## Figure

| Figura | Ruolo | Skill | Cosa presidia |
| ------ | ----- | ----- | ------------- |
| 👁️ Iris | Design Critic | `grl-agent-ui-critic` | Guarda una landing o una schermata e dice subito dove l'ha già vista: hero centrato in gradiente, tre card con icona, Inter a peso 600, blu-viola ovunque. |
| 🔎 Nora | SEO Strategist & Search Systems Auditor | `grl-agent-seo` | Distingue domanda, intento, crawl, indicizzazione, contenuto, dati strutturati e misurazione, verifica sempre live le regole SEO e trasforma ogni diagnosi in una modifica… |
| 📣 Dalia | Media Manager & Paid Advertising Strategist | `grl-agent-ads` | Trasforma un obiettivo commerciale in campagne pagate misurabili: Google Ads, Search, Performance Max, Display, YouTube e gli altri canali ADV entrano solo con destinatario,… |

## Skill e workflow

| Skill | Comando | Cosa fa |
| ----- | ------- | ------- |
| `grw-setup` | Installa Guardrails Web Experience | Registra Guardrails, le tre figure, le stanze tematiche di party mode e le voci di help. Non crea la memoria condivisa. |
| `grw-profile` | Profila il progetto | Raccoglie in pochi minuti gli otto campi che danno contesto a tutte e tre le figure, criticità inclusa. |
| `grw-profile` | Aggiorna il profilo | Riallinea il profilo quando il progetto cambia, e dice se il cambiamento invalida rischi già accettati. |
| `grw-board` | Convoca il collegio | Fa leggere lo stesso artefatto alle sole figure pertinenti e restituisce un riepilogo unico, conflitti compresi. |
| `grw-board` | Rischi già accettati | Mostra, raggruppato per figura, quello che il progetto ha consapevolmente scelto di accettare. |
| `grw-board` | Gate di rilascio | Verifica una release identificata e restituisce GO, GO_CON_CONDIZIONI, NO_GO o EVIDENZA_INSUFFICIENTE. |
| `grl-web` | Crea una landing o un sito | Dal brief di conversione — destinatario, promessa, obiezione, prova, azione — al mockup HTML a file singolo. |
| `grl-web` | Riprendi un mockup | Rientra su una pagina già fatta, applica il cambiamento e segnala se contraddice una decisione già registrata. |
| `grl-web` | Diagnostica una pagina | Perché una pagina che esiste già non converte: il brief ricostruito all'indietro e da tre a cinque mosse concrete. |
| `grl-web` | Promuovi a progetto | Dal mockup approvato al sito vero: Tailwind da CLI standalone, SEO, form, accessibilità, pronto per il deploy. |
| `grl-web` | Configura un sito vero | Prepara la scheda di un sito con parti condivise, contenuti che cambiano e animazioni; la scheda può poi passare a bmad-spec per essere trasformata in fette per bmad-build. |
| `grl-ads` | Audita account e campagne | Legge export e report, definisce il perimetro e ordina blocchi, distorsioni e opportunità senza modificare l'account. |
| `grl-ads` | Prepara un piano media | Dall'obiettivo alla struttura delle campagne, agli asset, al budget come scenario e al piano di misura. |
| `grl-ads` | Verifica tracking e consenso | Mappa eventi, conversioni, tag, fonte, consenso e verifiche senza caricare dati personali. |
| `grl-ads` | Ottimizza con change set | Confronta periodi compatibili e propone modifiche a campagne e budget con soglie, approvazione, dry-run e rollback. |
| `grl-ads` | Preflight della campagna | Controlla tracking, destinazione, claim, asset, policy, consenso, budget, autorizzazioni e rollback prima dell'azione. |
| `grl-ads` | Applica un change set | Esegue solo un'azione esplicitamente autorizzata, delimitata e validata; altrimenti resta in awaiting_approval o blocked. |
| `grl-automation` | Instrada un'automazione | Classifica lo scenario, sceglie agenti e workflow BMad e dichiara capability mancanti, scope e approvazioni. |
| `grl-automation` | Prepara un piano eseguibile | Costruisce passi idempotenti con input, output, precondizioni, rischio, approvazione e rollback. |
| `grl-automation` | Esegui controlli read-only | Raccoglie evidenze e confronti riproducibili senza modificare sistemi esterni. |
| `grl-automation` | Prepara un dry-run | Genera e valida diff o payload senza spendere, pubblicare o applicare side effect. |
| `grl-automation` | Esegui dopo approvazione | Applica solo lo scope approvato, registra prima/dopo e osserva il risultato; in caso di errore attiva il rollback. |
| `grl-automation` | Riprendi un'automazione | Riprende un run esistente dal primo passo non concluso senza duplicare scritture o side effect. |

## Installazione

```
bmad install grw
```

Poi, come primo passo, `grw-profile`: raccoglie il profilo di progetto — settore,
dati trattati, mercato, stack, criticità — e da lì ogni figura deriva quanto essere
severa. Senza profilo il default resta `normal` e le figure partono senza contesto.

## Memoria condivisa

Il profilo vive in `{project-root}/_bmad/memory/grl-shared/project-profile.md`, insieme
a `decisions.md` e `accepted-risks.md`. Il percorso è lo stesso per tutti i moduli
Guardrails: installandone due, il profilo resta uno solo e si compila una volta.

## Convivenza con il bundle

Questo modulo installa skill con **lo stesso nome** del bundle `grl` — `grl-agent-ui-critic`
sta identica in entrambi. Bundle e moduli tematici non vanno installati insieme nello
stesso progetto: si sceglie il bundle completo, oppure i moduli delle aree che servono.

## Stanze di party mode

grw-setup installa le stanze del modulo in `_bmad/custom/bmad-party-mode.toml`, senza cambiare la stanza di default:

- `bmad-party-mode --party grl-web`
- `bmad-party-mode --party grl-paid-media`
- `bmad-party-mode --party grl-automation`

## Licenza

MIT.

# Pensiero critico e IA

ClearLens è una palestra interattiva in italiano per aiutare studenti e docenti
a esaminare criticamente le risposte generate dall'intelligenza artificiale.

L'applicazione funziona nel browser e non richiede installazione. ClearLens non
memorizza i testi analizzati. Cyber Crisis può inviare nickname anonimo, codice
lezione, scelte e punteggi a un database Supabase configurato dal docente.

## Utilizzo

1. Scegliere una delle domande proposte o inserirne una nuova.
2. Porre la domanda a un assistente IA.
3. Incollare la risposta in ClearLens.
4. Analizzare possibili segnali di bias, carenze nelle prove e prospettive mancanti.
5. Utilizzare i prompt di approfondimento per mettere alla prova la risposta.

## Cyber Crisis

`gioco.html` contiene una simulazione con scenari di cybersecurity, rischi
dell'IA, AI Act e modello Cynefin. `admin.html` è l'area docente autenticata per
consultare i risultati anonimi ed esportarli in CSV.

La configurazione del database e delle policy di sicurezza è descritta in
`SUPABASE.md`.

> L'analisi è euristica e didattica: non determina automaticamente se una
> risposta è vera, falsa o discriminatoria.
